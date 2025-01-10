The website is built using the [Minimal Mistakes Jekyll theme](https://mmistakes.github.io/minimal-mistakes/). Below, I’ll guide you through the steps to create your own site using my modified version of the original theme.  

# Building Your Personal Site: A Simplified Guide  

This post is for anyone who wants to create a personal site but finds the process a bit challenging.  

This site is built using [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/), a Jekyll-based theme. I’ve explored several forks of this theme, such as [Academic Pages](https://academicpages.github.io), which are quite handy. However, I noticed that some functions were removed in these forks, making them harder to customize. So, I downloaded the [original ZIP file](https://mmistakes.github.io/minimal-mistakes/docs/installation/) and customized it myself.  

In this post, I’ll explain how I built my site, what changes I made, and how you can create your own. Exploring the forks I mentioned or figuring things out independently is always a rewarding experience! Let’s dive in.  

---

## Get Started  

### Option 1: Use My Template  
This is the easiest option since most of the work is already done for you. Simply download, clone, or fork this repository and customize it to suit your needs!
**[Download zip file](https://github.com/dizzyryan/site-template.github.io/archive/refs/heads/main.zip)**


### Option 2: Start from Scratch  

I’ll provide a brief overview here. For detailed instructions, refer to the [Minimal Mistakes documentation](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/).  

> [!NOTE]
> You can always follow the [original version and guidance](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/), which works perfectly fine.

#### Steps:  

1. Create a New GitHub Repository
    If you plan to use GitHub Pages to host your site, name your repository `<your-username>.github.io` and clone the repository to your local computer. 

    I personally host my website on [Vercel](https://vercel.com) because I’ve purchased a custom domain. Vercel offers free hosting for hobby projects or personal sites, making it an excellent alternative to GitHub Pages. 

    > [!CAUTION]
    > Hosting your repository publicly on GitHub might raise privacy concerns. While this typically isn’t an issue if you don’t mind, be cautious about exposing sensitive information. Alternatively, you can host your site on your personal server for enhanced security, though the process may differ from what I outline here. 

2. Download the Minimal Mistakes Theme

    > [!Note]
    > Since I made some changes to this theme, it's recommended to clone the original version if you plan to follow the steps outlined here.

    Clone or download the [Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/). Copy the following files into your repository:  
    - `_data`  
    - `_config.yml`  
    - `.gitignore`  
    - `index.html`  
    - `LICENSE` *(optional, for crediting the creator)*  
    - `Gemfile`

3. Edit the `Gemfile`
    Update the `Gemfile` by removing its contents and replacing them with the following:  
    ```
    source "https://rubygems.org"

    # Hello! This is where you manage which Jekyll version is used to run.
    # When you want to use a different version, change it below, save the
    # file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
    #
    #     bundle exec jekyll serve
    #
    # This will help ensure the proper Jekyll version is running.
    # Happy Jekylling!

    gem "github-pages", group: :jekyll_plugins
    gem "jekyll-include-cache", group: :jekyll_plugins
    gem "webrick"
    gem "erb" # For some reason not including this in Arch Linux breaks Jekyll dependencies

    # To upgrade, run `bundle update`.

    # gem "jekyll"
    # gem "minimal-mistakes-jekyll"

    # The following plugins are automatically loaded by the theme-gem:
    #   gem "jekyll-paginate"
    #   gem "jekyll-sitemap"
    #   gem "jekyll-gist"
    #   gem "jekyll-feed"
    #   gem "jekyll-include-cache"
    #
    # If you have any other plugins, put them here!
    # Cf. https://jekyllrb.com/docs/plugins/installation/
    group :jekyll_plugins do
      gem "jekyll-sitemap"
      gem "jemoji"
    end
    ```

4. Update Configuration
    * Uncomment and Update the Remote Theme
        Locate the line with `remote_theme` in `_config.yml`, uncomment it, and update it to the following:  
        ```
        remote_theme: "mmistakes/minimal-mistakes@4.26.2"
        ```  
    * Edit the Configuration**  
        Customize the configuration file to suit your site. For example, you can:  
        - Set your site’s name and description.  
        - Add a link to your GitHub repository.  

    For detailed instructions on all available options, refer to the [Minimal Mistakes configuration guide](https://mmistakes.github.io/minimal-mistakes/docs/configuration/).  

5. Preview Your Site Locally* 
    If you want to see how your site looks before pushing changes to GitHub, you can host it locally. This avoids the need to push your repo every time you make a modification. Follow these steps: 
    * Install Ruby and Jekyll
        Refer to the [Jekyll Documentation](https://jekyllrb.com/docs/) for installation instructions.  
    * Install Bundler
        Run the following command in your terminal:  
        ```
        gem install bundler
        ```
    * Install Dependencies
        Run `bundle install` in your terminal. If you skip this step, the terminal will prompt you to install the necessary dependencies when you proceed to the next step.
    * Host Your Site Locally
        Use the following command:  
        ```
        bundle exec jekyll serve
        ```
    * Preview Your Site
        Open your browser and go to `http://127.0.0.1:4000` to view your site.  

### Final Thoughts  

You’re almost done! The rest is up to you to figure out. Building your site can be an exciting journey. Debugging might be frustrating at times, but the satisfaction of seeing your final product come to life makes it all worth it. Good luck, and happy coding!  