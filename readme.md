<p align="center">
    <a href="https://yuay.ac.cn">
      <img src="https://s1.ax1x.com/2023/07/13/pCh4q9e.png" alt="pCh4q9e.png" border="0" /></a>
  </a>
</p>

# Yuay's Blog by Next.js Notion Starter Kit

## Intro

This repo is what I use to power my personal blog. [Yuay.ac.cn](https://yuay.ac.cn).

It uses Notion as a CMS, [react-notion-x](https://github.com/NotionX/react-notion-x), [Next.js](https://nextjs.org/), and [Vercel](https://vercel.com).Comments powered by [Utterances](https://utteranc.es/).


## Next.js Notion Starter Kit

- Setup only takes a few minutes ([single config file](./site.config.ts)) 💪
- Robust support for Notion content via [react-notion-x](https://github.com/NotionX/react-notion-x)
- Built using Next.js, TS, and React
- Excellent page speeds
- Smooth image previews
- Automatic social images
- Automatic pretty URLs
- Automatic table of contents
- Full support for dark mode
- Quick search via CMD+K / CMD+P
- Responsive for different devices
- Optimized for Next.js and Vercel
- ...

## Preview Images

<p align="center">
  <img alt="Example preview image" src="https://user-images.githubusercontent.com/552829/160142320-35343317-aa9e-4710-bcf7-67e5cdec586d.gif" width="458">
</p>

We use [next/image](https://nextjs.org/docs/api-reference/next/image) to serve images efficiently, with preview images optionally generated via [lqip-modern](https://github.com/transitive-bullshit/lqip-modern). This gives us extremely optimized image support for sexy smooth images.

### Redis

We use an external [Redis](https://redis.io) data store to cache generated preview images to speed up subsequent builds.
Redis provider： [Redis Labs](https://redis.com), they provides a free plan.

## Styles

All CSS styles that customize Notion content are located in [styles/notion.css](./styles/notion.css). They mainly target global CSS classes exported by react-notion-x [styles.css](https://github.com/NotionX/react-notion-x/blob/master/packages/react-notion-x/src/styles.css).

## Dark Mode

<p align="center">
  <img alt="Light Mode" src="https://transitive-bs.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F83ea9f0f-4761-4c0b-b53e-1913627975fc%2Ftransitivebullsh.it_-opt.jpg?table=block&id=ed7e8f60-c6d1-449e-840b-5c7762505c44&spaceId=fde5ac74-eea3-4527-8f00-4482710e1af3&width=2000&userId=&cache=v2" width="45%">
&nbsp; &nbsp; &nbsp; &nbsp;
  <img alt="Dark Mode" src="https://transitive-bs.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fc0839d6c-7141-48df-8afd-69b27fed84aa%2Ftransitivebullsh.it__(1)-opt.jpg?table=block&id=23b11fe5-d6df-422d-9674-39cf7f547523&spaceId=fde5ac74-eea3-4527-8f00-4482710e1af3&width=2000&userId=&cache=v2" width="45%">
</p>

Dark mode is fully supported and can be toggled via the sun / moon icon in the footer.

## Automatic Social Images

<p align="center">
  <img alt="Example social image" src="https://user-images.githubusercontent.com/552829/162001133-34d4cf24-123a-4569-a540-f683b22830d1.jpeg" width="600">
</p>

All Open Graph and social meta tags are generated from Notion content, which makes social sharing look professional by default.

Social images are generated automatically using [Vercel OG Image Generation](https://vercel.com/docs/concepts/functions/edge-functions/og-image-generation). Can tweak the default React template for social images by editing [api/social-images.tsx](./pages/api/social-image.tsx).

Can view an example social image live in production [here](https://www.yuay.ac.cn/api/social-image?id=3529877592df47afb437d25070e71bdb).

## Automatic Table of Contents

<p align="center">
  <img alt="Smooth ToC Scrollspy" src="https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fcb2df62d-9028-440b-964b-117711450921%2Ftoc2.gif?table=block&id=d7e9951b-289c-4ff2-8b82-b0a61fe260b1&cache=v2" width="240">
</p>

By default, every article page will have a table of contents displayed as an `aside` on desktop. It uses **scrollspy** logic to automatically update the current section as the user scrolls through your document, and makes it really easy to jump between different sections.

If a page has less than `minTableOfContentsItems` (default 3), the table of contents will be hidden. It is also hidden on the index page and if the browser window is too small.

This table of contents uses the same logic that Notion uses for its built-in Table of Contents block (see [getPageTableOfContents](https://github.com/NotionX/react-notion-x/blob/master/packages/notion-utils/src/get-page-table-of-contents.ts) for the underlying logic).

## Responsive

<p align="center">
  <img src="https://s1.ax1x.com/2023/07/13/pChotfO.md.jpg" alt="Mobile article pag" border="0" width="300" />
</p>


All pages are designed to be responsive across common device sizes.

## Comments
<p align="center">
  <img src="https://s1.ax1x.com/2023/07/13/pChor7t.md.png" alt="pChor7t.png" border="0" />
</p>

Comments powered by [Utterances](https://utteranc.es/).A lightweight comments widget built on GitHub issues. Use GitHub issues for blog comments.
Repository of comment data: [YuayYeonhi/comment](https://github.com/YuayYeonhi/comment)

## More...

More setup information can be found in the repository: [nextjs-notion-starter-kit](https://github.com/transitive-bullshit/nextjs-notion-starter-kit).
