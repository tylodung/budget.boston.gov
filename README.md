# budget.boston.gov

This is a basic Jekyll starter project. It uses Gulp for building everything, so that we can more easily incorporate things like BrowserSync, Stylus and any necessary plugins.

To get up and running, download (or fork) this repo. Then in your project run:

``` sh
bundle install
npm install
gulp
```

At this point, you should be able to visit `https://0.0.0.0:3000`.

---

To create custom pages, you can simply add reusable components to markdown files. 
> If you need to use the same component multiple times in the same file, you need to append the plus "+" character to the end of the key. An additional "+" needs to be added for each repeating component (e.g. to add a 3rd text_box use `text_box++:`).

Here's a short list of some common components you can use:

**Breadcrumbs**
![Screenshot of breadcrumb page navigation](/images/breadcrumbs.png "Breadcrumbs Screenshot")
```
breadcrumbs:
 - title: Home
   url: "/"
 - title: Dept
   url: "/departments"
 - current: Executive Summary
 - published: 2/15/17
```

---

**Intro**
![Screenshot of page introductory section](/images/intro.png "Intro Screenshot")

> Set sidebar_menu to false in order to have full spanning title, short description, and description sections

```
intro:
 - title: Executive Summary
   short_desc: >
     <div>"This budget is a manifestation of my vision for a
     Thriving, Healthy, and Innovative Boston."</div>
     <div>- Martin J. Walsh, Mayor</div>
   description: >
     Mayor Walsh presented a balanced budget that maintains 
     high levels of support in critical areas such as education 
     and public safety, makes limited strategic investments,
     continues the City's commitment to addressing its long-term
     liabilities, and builds on the Administration's record of 
     strong fiscal management. This is made possible by the 
     Administration's achievement of efficiencies and savings. 
     The City's data-driven managerial approach was recently 
     validated by the affirmation of Boston's triple A bond rating.
   sidebar_menu: true
```

---

**Text Block**
![Screenshot of a block of text component](/images/text_block.png "Text Block Screenshot")

> Omit the right_image key to have the text span the full screen

```
text_block:
  - title: Introduction
    body: >
      At the time Mayor Walsh took office, the City of Boston had successfully 
      weathered the storms of previous recessions. However, several major revenue
      sources never fully recovered, cost pressures continued to grow, and deferred
      investments persisted across City government. In its first two years, the 
      administration has systematically engaged in independent operational reviews
      and other planning efforts aimed at making government more efficient in order 
      to address areas needing renewed attention.
    right_image: http://tomakeawebsite.net/wp-content/uploads/2015/03/Google-charts-plugin.jpg
```

---

**Spanning Image**
![Screenshot of an image that spans the full screen](/images/spanning_image.png "Spanning Image Screenshot")
```
spanning_image:
  - title: Lorem ipsum title
    desc: This is the description for the spanning image
    link:
      - text: Click Here
        url: https://google.com
    src: https://www.boston.gov/sites/default/files/styles/resp_wide_2000x800custom_boston_wide_1x/public/winter_swimming_10.jpg?itok=W91jOE5G&timestamp=1452037695
    alt: Placeholder alt text
    title: Placeholder image title
```
---

**JS Table**
![Screenshot of a table that pulls data from a JSON source](/images/js_table.png "JS Table Screenshot")

```
js_table:
  - title: Remote JSON
    json_source_url: "http://mysafeinfo.com/api/data?list=presidents&format=json"
    columns:
      - column_name: Name
        json_key: nm
      - column_name: Party
        json_key: pp
      - column_name: Term
        json_key: tm
  - title: Local JSON
    json_source_url: "http://localhost:3000/test.json"
    columns:
      - column_name: Name
        json_key: nm
      - column_name: Party
        json_key: pp
      - column_name: Term
        json_key: tm
      - column_name: Custom
        json_key: custom
  - title: 2nd Local test
    json_source_url: "http://localhost:3000/test2.json"
    columns:
      - column_name: New title
        json_key: this thing
      - column_name: Name
        json_key: nombre
      - column_name: Other
        json_key: other thing
      - column_name: Last Col
        json_key: custom
```
