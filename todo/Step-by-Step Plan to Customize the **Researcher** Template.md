


1. **Fork and Set Up the Jekyll Template**  
    Begin by forking or downloading the **Researcher** Jekyll template from GitHub[github.com](https://github.com/ankitsultana/researcher#:~:text=Installation). This gives you a personal copy to modify. If you plan to host on GitHub Pages, you can rename the repository to `<your-username>.github.io` (or your custom domain repo) so that it serves as your website. Make sure you have a Jekyll environment set up locally (Ruby and Jekyll gem) if you want to preview changes on your machine. Otherwise, you can rely on GitHub Pages to build the site after you push changes.
    
2. **Configure Site Settings (_config.yml)**  
    Open the `_config.yml` file in the repository and update the basic site settings:
    
    - **Title**: Set the `title` field to your name or desired site title (for example, your name or "_PhD in AI for Health_"). This title typically appears as the main heading of the site[github.com](https://github.com/ankitsultana/researcher#:~:text=,config.yml).
        
    - **URL and Base URL**: If using GitHub Pages without a custom domain, set `url` to `https://<your-username>.github.io` (or your custom domain if you have one) and set `baseurl` to `""` (empty) since the site will be at the root. The template’s default baseurl might be “/researcher”, which you should remove or change to match your deployment path. This ensures your navigation links work correctly.
        
    - **Navigation Menu**: Edit the navigation links under the `nav:` section to fit your site. For example, you might keep an **About** link (pointing to the homepage or a dedicated about page), a **Publications** or **Resume** link, a **Contact** link, and add a **Blog** link. You can use the example in the template’s README as a guide[github.com](https://github.com/ankitsultana/researcher#:~:text=,For%20example). For instance:
        
        yaml
        
        CopyEdit
        
        `nav:  - name: "About"    link: "/"          # assuming baseurl is empty for root  - name: "Blog"    link: "/blog"      # link to a blog page you'll create  - name: "Resume"    link: "resume.pdf" # if you have a resume/CV PDF  - name: "Contact"    link: "/contact"`
        
        Adjust or remove items as needed (if you don’t have a resume PDF yet, you can omit that for now).
        
    - **Theme Color/Style**: The template uses a clean, grey-toned monospace design by default. Since you indicated the default grey is fine, you do not need to change the color scheme. (If you ever want to tweak the accent color of hyperlinks, you could edit the `accent` variable in `_sass/vars.scss`[github.com](https://github.com/ankitsultana/researcher#:~:text=,sass%2Fvars.scss), but we'll keep it as is.)
        
    - **Analytics (Optional)**: If you have Google Analytics or similar, you can set the `tracking_id` in `_config.yml` (this is optional and can be skipped for now).
        
    - **Institute Logo (Optional)**: The template supports adding an institute logo at the top (via an `ins_logo`config and an image file)[github.com](https://github.com/ankitsultana/researcher#:~:text=,to%20the%20desired%20value). If you want to display an Imperial College logo or another logo, you can add the image and set `ins_logo: "/path/to/your-logo.png"` in the config. This step is optional; it’s fine to skip if you prefer a simple look.
        
3. **Add Your "About Me" Information**  
    The main content of the homepage (or the About page) is written in Markdown (see `index.md`). Open `index.md`and replace the placeholder **About Me** section with your own biographical info. Use the text you provided, for example:
    
    markdown
    
    CopyEdit
    
    `## About Me  I'm a PhD student in AI for Health at Imperial College London.   I'm working on building [Singularity Health](https://www.singularity-health.io), an AI search tool for retrieving medical data. I completed my medical degree in 2019 and worked as a doctor in the NHS for 5 years (2019–2024).`
    
    Make sure to format the Singularity Health mention as a hyperlink (as shown above) so that visitors can click through to `singularity-health.io`. The template’s default text had a casual introduction — you can replace it entirely with your professional bio. Keep the tone and length appropriate for a personal academic webpage (the example you gave is concise and fits well). If you want this section to appear on the home page, ensure the navigation link for "About" (or "Home") points to the correct location (we used the homepage `/`). Save the changes to `index.md` after adding your info.
    
4. **Customize Additional Sections (Research Interests, etc.)**  
    The template might include other sections in `index.md` by default, such as **Research Interest** or placeholders for skills, etc. Review the content below your About Me in `index.md` (for example, a "## Research Interest" section with lorem ipsum text[github.com](https://github.com/ankitsultana/researcher/blob/gh-pages/index.md#:~:text=Research%20Interest), and a sample **Publications** list). Update or remove these sections as needed:
    
    - **Research Interests**: If applicable, replace the dummy text under "Research Interest" with a brief description of your academic interests. For example, you could write a few sentences about your focus in _AI for healthcare_, your specific research questions, or the intersection of medicine and machine learning that you are passionate about. If you feel your **About Me** already covers this, you could instead remove this section entirely to avoid redundancy. The site is yours to structure, so include the sections you find relevant.
        
    - **Education/Experience**: You mentioned your medical degree and NHS work in the About Me paragraph. Some people prefer to list education and work experience in separate sections (like a mini-resume). If you want, you can add a **Education** or **Experience** section in the Markdown, listing your degrees (e.g., _MBBS, 2019, XYZ University_) and roles (_Foundation Doctor, NHS, 2019–2024_). This is optional – since the template is a "resume" style, it can accommodate such lists, but it’s up to you if you want that detail on the page or just keep it narrative.
        
    - **Contact Info**: The template comes with a `contact.md` page. Open `contact.md` and update it with your contact details. Typically, you might include your email address (you can format it as a mailto link), and any social media or professional profiles. For example, you can list your Twitter (X) handle, LinkedIn, GitHub, etc., with hyperlinks. You might format it in Markdown or HTML with icons. _Tip:_ You can use Font Awesome icons (if included or added to the site) or simple text links. For instance:
        
        markdown
        
        CopyEdit
        
        `- Email: [youremail@domain.com](mailto:youremail@domain.com)   - GitHub: [YourUsername](https://github.com/YourUsername)   - LinkedIn: [Your Name](https://www.linkedin.com/in/your-profile)`  
        
        Ensure the "Contact" link in your nav (configured in Step 2) points to this contact page (e.g., `/contact`). If you prefer not to have a separate contact page, you could also integrate contact info in the footer or sidebar of the main page.
        
    - **Profile Picture**: If you have a profile picture or avatar you’d like to display, add the image file to the repository (e.g., in the root or an `assets/` folder). Then insert an image tag in the Markdown where you want the picture to appear. The template recommends giving it a special class for styling – for example, at the top of your About Me section:
        
        html
        
        CopyEdit
        
        `<img class="profile-picture" src="your-photo.jpg" alt="Profile picture">`
        
        This will ensure the image is styled appropriately (the template’s example uses a circular cropped style for class `profile-picture`[github.com](https://github.com/ankitsultana/researcher#:~:text=,other%20words%2Cdo%20it%20like%20so)). Make sure to reference the correct path to your image. This step is optional, but a photo can add a personal touch.
        
5. **Populate the Publications Section from Google Scholar**  
    A key part of your site will be the **Publications** section. Instead of manually typing out each publication, you decided to populate this using your Google Scholar profile data. Here’s how to do that:
    
    - **Export your Google Scholar citations**: Go to your Google Scholar profile and export your publication list. Google Scholar allows you to select multiple entries and then export them. Choose a format that can be easily parsed; for our purpose a CSV format is convenient (a spreadsheet of your publications). For instance, in Scholar you might use the _“Export”_ option or Google’s _“My library”_ to get a CSV of all publications. If Scholar doesn’t provide a direct CSV, you can export to BibTeX, or use a tool like Publish or Perish to get a CSV. The goal is to have a file (say `citations.csv`) that lists all your publications with details (title, authors, year, etc.).
        
    - **Add the data to your site**: Place the CSV file in your Jekyll site’s `_data/` directory (create the `_data`folder if it doesn’t exist). Name the file something like `citations.csv`. Jekyll can easily read data files in this folder.
        
    - **Use a Jekyll include to generate the publication list**: Instead of writing raw Markdown for each paper, you can use a ready-made include script that reads the CSV and outputs a formatted list of citations. One such solution is provided by C. McComb’s Google Scholar include filecmccomb.com. Download the `publications.html` include from that resource (available on GitHub as mentioned in the blog) and put it in your `_includes/` directory. This include will automatically format your publication list in a chosen citation style.
        
    - **Insert the include in your page**: In `index.md`, find the **Publications** section (the template has an example list item). Remove the placeholder item and instead use the include. For example, you can write:
        
        liquid
        
        CopyEdit
        
        `{% include publications author="YourLastName" %}`
        
        This will include all entries from `citations.csv` and format them. You can adjust parameters (like author filter or citation style) as needed – the include supports APA/MLA/etc and filtering by author namecmccomb.comcmccomb.com. If you want all publications listed, a simple `{% include publications %}` will list everythingcmccomb.com.
        
    - **Verify formatting**: After integrating, build your site to ensure the publications are listed correctly (they should appear as a numbered list of citations in your chosen style). The include method saves you from manually updating the list; in the future, you can just update the CSV file when you have new publications. _(Alternatively:_ If you prefer not to use a CSV/include, you can manually enter your publications in a Markdown list under the Publications section. Each item can be formatted as “**Author names (Year). Title. Venue.**” etc. This is simpler but requires manual upkeep. Since you specifically requested using Scholar, the above CSV method automates the process.)*
        
6. **Add a Blog Section for Your Posts**  
    You mentioned wanting the blog directly on your website (as opposed to an external blog), which means we’ll set up the Jekyll blog functionality within this template. Jekyll supports blog posts out-of-the-box[jekyllrb.com](https://jekyllrb.com/docs/posts/#:~:text=Blogging%20is%20baked%20into%20Jekyll,turn%20it%20into%20a%20blog), even if the template is resume-oriented. Here are the steps:
    
    - **Create a `_posts` folder**: In the root of your repository, create a directory named `_posts` (if it’s not already there). This is where all your blog post files will live[jekyllrb.com](https://jekyllrb.com/docs/posts/#:~:text=The%20,Markdown%2C%20HTML%20is%20also%20supported). Each post is a Markdown file with a filename format of `YYYY-MM-DD-title.md` (year-month-day at the start)[jekyllrb.com](https://jekyllrb.com/docs/posts/#:~:text=To%20create%20a%20post%2C%20add,directory%20with%20the%20following%20format). For example, a post from July 24, 2025 could be named `2025-07-24-welcome-to-my-blog.md`.
        
    - **Write a blog post**: Inside `_posts`, create your first post file with the naming convention above. At the top of the file, include Jekyll **front matter** (between `---` lines). For example:
        
        markdown
        
        CopyEdit
        
        `--- layout: default title: "Welcome to My Blog" date: 2025-07-24 tags: [AI, healthcare]   # (optional tags) ---  # Welcome to My Blog  This is my first post on my personal site. I plan to share insights on AI for healthcare, medical learning, and more here.`
        
        In the front matter, we set `layout: default` to use the site’s default page layout (you could create a custom `post` layout, but using the default ensures the style is consistent). Set the `title` to the post title and include a `date`. You can add `tags` or `categories` if you want to organize posts by topics (e.g., tags like `Medicine` or `AI`). Write the content of your post in Markdown below the front matter. Save the file.
        
    - **Create a Blog index page**: Next, make a page that will list all your blog posts. You can do this by creating a new Markdown file in the root (e.g., `blog.md`). In `blog.md`, add front matter and a posts loop:
        
        markdown
        
        CopyEdit
        
        `--- layout: default title: "Blog" permalink: /blog/ --- ## Blog Posts <ul>   {% for post in site.posts %}     <li>       <a href="{{ post.url }}">{{ post.title }}</a> <small>({{ post.date | date: "%B %d, %Y" }})</small>     </li>   {% endfor %} </ul>`
        
        This uses a Liquid loop to go through all posts and list them as links[jekyllrb.com](https://jekyllrb.com/docs/posts/#:~:text=Creating%20an%20index%20of%20posts,links%20to%20your%20blog%20posts). The `permalink: /blog/`in the front matter ensures the page is accessible at `yourdomain/blog/`. You can style this list or add excerpts as desired, but the above is a simple listing of post titles and dates.
        
    - **Add “Blog” to navigation**: As mentioned in Step 2, ensure you've added an entry in `_config.yml`'s `nav`for the Blog. For example, if your blog index page is `blog.md` with permalink `/blog/`, your nav config should include:
        
        yaml
        
        CopyEdit
        
        `- name: "Blog"   link: "/blog"`
        
        This will show a "Blog" link in the top menu that points to your posts page. Now your blog posts are fully integrated into your website – you can write new Markdown files in `_posts` for each article or essay you want to publish, and they will appear on this page automatically (sorted by date, newest first by default).
        
7. **Test Your Site and Deploy**  
    With content in place (About me, publications, blog, etc.), you should test the site to make sure everything looks correct:
    
    - **Local Preview**: If you have Ruby and Jekyll set up locally, run `jekyll serve` (or `bundle exec jekyll serve` if using Bundler) in the project directory. Open `http://localhost:4000` in your browser to view the site. Check that the About Me section displays your info (with the Singularity Health link working), the Publications section is populated with your papers, and the Blog page lists your posts. Verify that all navigation links work (click through About, Blog, Contact, etc.). Adjust content or formatting as needed. For example, you might tweak text length, add line breaks, or fix any formatting issues you spot during preview.
        
    - **Deploy on GitHub Pages**: Once you are satisfied, push your changes to GitHub. If using GitHub Pages, ensure the repository is properly configured (for a user site repository named `<username>.github.io`, Pages will auto-deploy from the main branch by default; for a project page, you might need to enable Pages in the repo settings and set the branch). After a few minutes, your site should be live at the configured URL. Visit your website URL to double-check everything is live.
        
    - **Custom Domain (if applicable)**: If you plan to use a custom domain (like a personal .io or .com domain), add a `CNAME` file in the repository with your domain, and configure the DNS to point to GitHub Pages. This is an extra step outside the template customization, but worth noting if you want `www.yourdomain.com` for your site.
        
    - **Post-Deployment Review**: Finally, review the live site. Check that the **default grey theme** and overall styling looks good to you. The template’s minimalist design should highlight your content. If something appears off (e.g., broken links, missing images), go back to your code to fix the path or configuration and redeploy. Once everything looks good, your site is up and running with your updated template!
        
8. **Maintenance and Updates**  
    Going forward, keep your website updated by editing the Markdown files:
    
    - To add a new blog post, simply create a new file in `_posts` and it will show up on the Blog page after you deploy.
        
    - To add new publications, update your Google Scholar and regenerate the `citations.csv` (or add the new entry manually to the CSV) and re-deploy – the list will update accordingly.
        
    - Update your About Me or other sections as your career progresses (for example, when you finish your PhD or start new projects). Because everything is Markdown or simple config, maintenance is straightforward.
        
    - If the template itself gets updated (since it's a fork, the original might have improvements), you can consider pulling in updates, but note that any heavy customization you do might make merging template updates tricky. In most cases, the site will not need frequent template changes, so this is optional.