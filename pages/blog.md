---
layout: default
title: Blog
permalink: /blog
---

<style>
  body {
    font-family: 'Arial', sans-serif;
    color: #333;
    background-color: #f4f4f4;
  }

  .blog-container {
    margin: 20px auto;
    max-width: 800px;
    padding: 20px;
  }

  .blog-unit {
    margin: 20px 0;
    padding: 20px;
    border-radius: 10px;
    background-color: #f9f9f9;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  .blog-unit h1 {
    font-size: 2em;
    margin-bottom: 10px;
    color: #6e8efb;
  }

  .blog-unit h1 a {
    text-decoration: none;
    color: #6e8efb;
  }

  .blog-unit h1 a:hover {
    text-decoration: underline;
    color: #a777e3;
  }

  .blog-date {
    color: #999;
    font-size: 0.9em;
    margin-bottom: 15px;
  }

  .blog-unit p {
    margin: 15px 0;
    line-height: 1.6;
  }

  .blog-buttons {
    display: flex;
    justify-content: flex-end;
    margin-top: 15px;
  }

  .blog-buttons button {
    margin-left: 10px;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s;
  }

  .edit-button {
    background-color: #a777e3;
    color: white;
  }

  .edit-button:hover {
    background-color: #9d6bd5;
  }

  .delete-button {
    background-color: #f44336;
    color: white;
  }

  .delete-button:hover {
    background-color: #e53935;
  }

  .edit-form {
    display: flex;
    flex-direction: column;
    margin-top: 20px;
  }

  .edit-form input,
  .edit-form textarea {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 1em;
  }

  .edit-form button {
    width: 100%;
    padding: 10px;
    margin-top: 10px;
    background-color: #6e8efb;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s;
  }

  .edit-form button:hover {
    background-color: #4b68e4;
  }

  .edit-form .cancel-edit-button {
    background-color: #f44336;
  }

  .edit-form .cancel-edit-button:hover {
    background-color: #e53935;
  }
</style>

<section>
  <div class="blog-container" id="blog-container">
    <!-- 블로그 포스트가 여기에 동적으로 추가됩니다. -->
  </div>
</section>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
<script>
  $(document).ready(function () {
    function loadPosts() {
      $.ajax({
        url: "https://tododebackend.fly.dev/api/v1/posts",
        method: "GET",
        success: function (response) {
          const posts = response.data;
          const blogContainer = $("#blog-container");
          blogContainer.empty();

          posts.forEach((post) => {
            const postElement = $(`
              <div class="blog-unit" data-id="${post.id}">
                <h1><a href="#">${post.title}</a></h1>
                <span class="blog-date">
                  ${new Date(post.created_date).toLocaleDateString("ko-KR", {
                    year: "numeric",
                    month: "long",
                    day: "numeric",
                  })}
                </span>
                <p>${post.content}</p>
                <div class="blog-buttons">
                  <button class="edit-button">Edit</button>
                  <button class="delete-button">Delete</button>
                </div>
              </div>
            `);
            blogContainer.append(postElement);
          });

          $(".edit-button").click(function () {
            const postId = $(this).closest(".blog-unit").data("id");
            const postTitle = $(this).closest(".blog-unit").find("h1 a").text();
            const postContent = $(this).closest(".blog-unit").find("p").text();

            const editForm = $(`
              <div class="edit-form">
                <input type="text" class="edit-title" value="${postTitle}" required />
                <textarea class="edit-content" rows="10" required>${postContent}</textarea>
                <button class="save-edit-button">Save</button>
                <button class="cancel-edit-button">Cancel</button>
              </div>
            `);

            $(this).closest(".blog-unit").html(editForm);

            $(".save-edit-button").click(function () {
              const newTitle = $(this).siblings(".edit-title").val();
              const newContent = $(this).siblings(".edit-content").val();

              $.ajax({
                url: `https://tododebackend.fly.dev/api/v1/posts/${postId}`,
                method: "PATCH",
                contentType: "application/json",
                data: JSON.stringify({ title: newTitle, content: newContent }),
                success: function () {
                  alert("Post updated successfully!");
                  loadPosts();
                },
                error: function (err) {
                  console.error("Error updating post:", err);
                  alert("Failed to update post.");
                },
              });
            });

            $(".cancel-edit-button").click(function () {
              loadPosts();
            });
          });

          $(".delete-button").click(function () {
            const postId = $(this).closest(".blog-unit").data("id");

            if (confirm("Are you sure you want to delete this post?")) {
              $.ajax({
                url: `https://tododebackend.fly.dev/api/v1/posts/${postId}`,
                method: "DELETE",
                success: function () {
                  alert("Post deleted successfully!");
                  loadPosts();
                },
                error: function (err) {
                  console.error("Error deleting post:", err);
                  alert("Failed to delete post.");
                },
              });
            }
          });
        },
        error: function (err) {
          console.error("Error fetching posts:", err);
          alert("Failed to fetch posts.");
        },
      });
    }

    loadPosts();
  });
</script>
