<?php
/* 
Plugin Name: JMS Rss Feed
Plugin URI: https://jmsliu.com/products/jms-rss-feed/
Description: Adds the featured image tag <jms-featured-image> to your posts to the RSS feed.
Author: James Liu
Version: 3.5.0
Author URI: https://jmsliu.com/
License: GPL2

{Plugin Name} is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 2 of the License, or
any later version.
 
{Plugin Name} is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.
 
You should have received a copy of the GNU General Public License
along with {Plugin Name}. If not, see {License URI}.
*/

	global $jms_rss_db_version;
	$jms_rss_db_version = '1.0';

	add_action('rss2_item', 'add_jms_img_rss_node');

	function add_jms_img_rss_node() {
		global $post;
		if(has_post_thumbnail($post->ID)) {
			$thumbnail = wp_get_attachment_image_src(get_post_thumbnail_id($post->ID), "full");
			echo "<jms-featured-image>".$thumbnail[0]."</jms-featured-image>";
		}
	}
?>