# Retro Forum

Retro Forum is a web application that displays posts from a forum. The application allows users to load, view, and interact with posts. 
# live link
netlify live link:https://retro-forum-using-api.netlify.app/

## Features

### Load All Posts
- The application fetches all posts from the API endpoint `https://openapi.programming-hero.com/api/retro-forum/posts` and displays them on the homepage.
- Each post card includes:
  - An active status indicator
  - Post image
  - Category and author information
  - Post title and description
  - Comment count, view count, and posted time
  - A "Mark as Read" button

### Search Posts by Category
- Users can search for posts by category using a search box.
- The application fetches posts matching the category from the API endpoint `https://openapi.programming-hero.com/api/retro-forum/posts?category={categoryID}` and displays them.

### Load Latest Posts
- The application fetches the latest posts from the API endpoint `https://openapi.programming-hero.com/api/retro-forum/latest-posts`.
- Each latest post card includes:
  - Cover image
  - Post title and truncated description
  - Author information including profile image and designation
  - A "See more" button to toggle the full description

### Mark Posts as Read
- Users can mark posts as read by clicking the "Mark as Read" button.
- The title and view count of the marked posts are displayed in the "Read Posts" section.
- The count of read posts is updated dynamically.

### Loading Spinner
- A loading spinner is shown while the data is being fetched from the API.

## Usage

### Loading All Posts
The function `loadAllPosts` fetches all posts from the API and calls `displayAllPosts` to render them.

### Displaying All Posts
The function `displayAllPosts` creates HTML elements for each post and appends them to the container `all-posts-container`.

### Searching Posts by Category
The function `getPostByCategories` gets the search text and calls `displayPostByCategories` to fetch and display posts by category.

### Displaying Latest Posts
The function `loadLatestPosts` fetches the latest posts from the API and calls `displayLatestPosts` to render them.

### Marking Posts as Read
The function `markAsRead` increments the read posts count and updates the "Read Posts" section with the title and view count of the marked post.

### Toggling Description
The function `toggleDescription` toggles the display of the full description for the latest posts.

### Handling Loading Spinner
The function `toggleLoadingSpinner` shows or hides the loading spinner based on the `isLoading` state.

