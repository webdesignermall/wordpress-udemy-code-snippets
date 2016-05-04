# wordpress-udemy-hook-snippets
This is the entire collection of PHP code snippets supporting the online course titled "WordPress Developer's Cookbook" course on Udemy at https://www.udemy.com/wordpress-developer-cookbook. The snippets contain most action and filter hooks for various WordPress functionality including, but not limited to:
- user management
- admin
- post loops
- and more

Currently, there are over 30 videos and the goal is to have over 100 WordPress videos and snippets by July 1, 2016.

Students can download these scripts as a whole instead of with each video to add to their WordPress plugins and themes. 

For students who are taking this course and who wish to make changes to any of the snippets, please submit a pull request for consideration to be featured in the course.

To use these snippets:

1. Rename any of the .txt files to .php
2. Add those code to your WordPress plugins or your functions.php file of your WordPress theme.
3. Please follow the instructions in the videos in the course.

Avoiding Collisions With Other PHP Scripts

Since WordPress is written in PHP, it is possible that using these hooks may contain callback functions that are identical to other callback functions in your WordPress plugins and themes. If that is the case, you can change the name of your callback function to any other name. Otherwise, you will receive a PHP error "function is already defined."

Also to repair this issue, change the reference function to the new callback function name. 

For example, if your hook is this:

add_action('login_head','change_logo');
function change_logo()
{
	//PHP code
}

There may already be a PHP function called change_logo in a different plugin. Simply change your callback function to anything else like:

add_action('login_head','change_new_logo_to_login_form');
function change_new_logo_to_login_form()
{
	//PHP code
}

Also descriptions about what these hook snippets go are also along with each video in the course at https://www.udemy.com/wordpress-developer-cookbook.