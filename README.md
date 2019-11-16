# Prepmaster
Crawls RSS feeds and stores webpages that are linked. Useful for the Extemporaneous Speaking Event of Speech and Debate

## Entering RSS sources
- In `links.txt`, add links to raw XML RSS feeds from various News sites such as:
```
# Huffington Post Sources
Huffington Post Front Page	https://www.huffpost.com/section/front-page/feed
Huffington Post Politics	https://www.huffpost.com/section/politics/feed

# The Guardian Sources:
# Enter sources here
```
- Lines beginning with "#" or empty lines are not interpreted
- Each line should contain the title of the feed (which will be the name of the folder) and the link to the RSS feed, seperated by a tab
- While the title is not neccessary, it is strongly recommended. You may enter just the link

## What it does
- When you set up the `links.txt` file and run the `BaliGenie.py` script, the program crawls the RSS feeds to fetch any webpages it links to
- It saves every link it finds to the `res` folder under in the date it was accessed under the source it was found from
- There will be a `cache.txt` file in the res folder that will be automatically generated
- This file enters every link the program accessed, so if the same link is accessed multiple times it will not create duplicate files
- Links in the cache expire every week, i.e. files may repeat if the RSS feed does not change its articles in a week (these should be updated daily or even more frequently)
- To keep the article base updated you should run the script regularly, ideally automatically on a set frequency
