---
layout: default
title: New Post
permalink: /post
---

<style>
  .form-container {
    margin: 20px auto;
    max-width: 600px;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }

  .form-container h2 {
    margin-bottom: 20px;
    font-size: 1.8em;
    color: black;
    text-align: center;
  }

  .form-container input,
  .form-container textarea {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 1em;
  }

  .form-container button {
    width: 100%;
    padding: 10px;
    margin-top: 10px;
    background: linear-gradient(135deg, #6e8efb, #a777e3);
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s;
  }

  .form-container button:hover {
    background: linear-gradient(135deg, #6e8efb, #a777e3);
  }
</style>

<div class="form-container">
  <h2>새 글 작성하기</h2>
  <form id="blog-post-form">
    <input type="text" id="title" name="title" placeholder="Title" required />
    <textarea id="content" name="content" rows="10" placeholder="Content" required></textarea>
    <button type="submit">Submit</button>
  </form>
</div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
<script>
  $(document).ready(function () {
    $("#blog-post-form").submit(function (event) {
      event.preventDefault();
      const postData = {
        title: $("#title").val(),
        content: $("#content").val(),
      };

      $.ajax({
        url: "https://tododebackend.fly.dev/api/v1/posts",
        method: "POST",
        contentType: "application/json",
        data: JSON.stringify(postData),
        success: function (data) {
          alert("Post created successfully!");
          $("#title").val('');
          $("#content").val('');
        },
        error: function (err) {
          console.error("Error creating post:", err);
          alert("Failed to create post.");
        },
      });
    });
  });
</script>
