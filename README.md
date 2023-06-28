**Multiple-Choice Questions:**

1. What is WordPress?
   - [X] a) A content management system (CMS)
   - [ ] b) A programming language
   - [ ] c) An operating system
   - [ ] d) A database management system

2. Which file is responsible for displaying the content of a single blog post in WordPress?
   - [X] a) single.php
   - [ ] b) page.php
   - [ ] c) archive.php
   - [ ] d) index.php

3. Which of the following hooks is executed after a new user is registered in WordPress?
   - [ ] a) init
   - [ ] b) wp_login
   - [X] c) wp_insert_user
   - [ ] d) wp_enqueue_scripts

4. What is the correct way to enqueue a JavaScript file in WordPress?
   - [ ] a) add_script()
   - [ ] b) enqueue_script()
   - [X] c) wp_enqueue_script()
   - [ ] d) include_script()

5. What is the purpose of the functions.php file in a WordPress theme?
   - [ ] a) To define custom post types
   - [ ] b) To add custom CSS styles
   - [X] c) To add custom PHP functions
   - [ ] d) To create template files

6. Which function can be used to retrieve the URL of the site's homepage in WordPress?
   - [ ] a) get_permalink()
   - [X] b) get_home_url()
   - [ ] c) get_site_url()
   - [ ] d) home_url()

7. Which database table stores WordPress plugin settings?
   - [ ] a) wp_posts
   - [X] b) wp_options
   - [ ] c) wp_users
   - [ ] d) wp_meta

8. What is the purpose of the `wp_head()` function in a WordPress theme?
   - [ ] a) It displays the site's header content.
   - [ ] b) It registers custom post types.
   - [X] c) It loads JavaScript files.
   - [ ] d) It generates the site's footer.

9. Which function can be used to retrieve the title of the current WordPress post or page?
   - [ ] a) get_the_content()
   - [ ] b) the_title()
   - [X] c) get_the_title()
   - [ ] d) the_content()

10. How can you add a custom menu location in a WordPress theme?
    - [ ] a) By adding a menu widget to a sidebar
    - [X] b) By using the `register_nav_menu()` function in the theme's functions.php file
    - [ ] c) By modifying the style.css file
    - [ ] d) By installing a menu plugin

**Code Challenge:**

Write a function in PHP that takes an

 array of post IDs as input and returns an array of their corresponding post titles. Use the WordPress function `get_the_title()` to retrieve the title of each post.

```php
function get_post_titles(array $post_ids): array {
    $post_titles = [];

    foreach ($post_ids as $post_id) {
        $post = get_post($post_id);
        if ($post) {
            $post_titles[] = get_the_title($post);
        }
    }

    return $post_titles;
}
```

