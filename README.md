# AgentLens Social Importer

**Save what inspires you, wherever it lives.**

**Keep the inspiration. Keep the source.** Save selected images and videos from supported social posts and creator profiles to Eagle, together with original post links and available creator details, captions, and publication dates.

Preview a single post or browse creator-profile results, then choose what to import. Source information is recorded with the media, so visual references and their context stay together in your library.

[Install from Eagle Plugin Center](https://community-en.eagle.cool/plugin/776389a1-2351-46f0-8174-a8d7e7996be5) · [Quick start](#quick-start) · [Account and credits](#account-and-credits)

> Requires Eagle 4.0 or later, an internet connection, and an AgentLens account. Sign-in is required for live URL fetching. Access depends on account eligibility, an active plan, and available fetch credits.

## 🖼 Choose the media worth keeping

- **Single-post fetch:** retrieve available images and videos from a supported post, including multiple media items when the service returns them.
- **Creator-profile bulk fetch:** review returned posts from a supported creator profile and select media to import. Load more results when available.
- **Preview before importing:** inspect the returned media and source information before choosing files.
- **Organize as you save:** adjust filenames and tags, then choose an Eagle destination folder.
- **Source information recorded on import:** keep the original post URL and available creator details, captions, and publication dates with the selected files.

These are manual fetching workflows. Auto-Fetch and scheduled creator monitoring are not included in this release.

## Installation

1. Open Eagle's **Plugin Center** and search for **AgentLens Social Importer**.
2. Install the plugin.
3. Open it from Eagle's **Plugins** menu.

You can also open the [official Eagle Community listing](https://community-en.eagle.cool/plugin/776389a1-2351-46f0-8174-a8d7e7996be5).

## Quick start

### 1. Connect your account

Start sign-in from the plugin, complete the AgentLens website's authorization flow, and return to Eagle. Check that your account is connected and has access and credits for your requested operation.

### 2. Fetch a post or creator profile

For one post, choose **Single post fetch**, paste a supported post URL, and click **Parse**.

For several posts, choose **Creator profile bulk fetch**, paste a supported creator profile URL, and click **Parse**. Review the returned results. Use **Fetch More** when more results are available; additional fetching may consume credits.

### 3. Review and import

1. Select the images or videos you want to keep.
2. Review source details and adjust filenames or tags if needed.
3. Choose a destination folder and start the import.
4. Keep Eagle running until the operation finishes, then review the import result and the saved files.

A successful parse means that results were retrieved. Check the import result separately to confirm which files reached your library.

## 🏷 What gets saved

Selected images and videos become media files in your Eagle library. When the source information is available:

- **Filename:** a readable name following the pattern below.
- **Website field:** the original post URL.
- **Annotation:** platform, creator name or ID, creator profile URL, publication date, and caption. If there is no caption, the title is used instead; both are not written together.
- **Tags:** tags you use to organize and search your collection.

```text
[Platform]_[Creator name or ID]_[Post date]_[first 10 words of title or caption]_[sequence]
```

Available fields depend on the source. An original post can change or disappear; successfully imported local files remain in your library.

## Supported platforms

Supported links are recognized from Pinterest, Instagram, TikTok, X (Twitter), Xiaohongshu, Douyin, WeChat Channels, Facebook, Threads, Bluesky, Lemon8, Weibo, and Kuaishou.

Support varies by platform, URL type, and media availability. Post support does not guarantee profile support. Bulk fetching does not promise every historical post or every media item from a creator.

A URL that works in your signed-in browser may be unavailable to AgentLens API. Private, deleted, login-only, or otherwise restricted content is not guaranteed to work.

## Account and credits

Live content retrieval is provided by [AgentLens API](https://agentlensapi.io/). It requires an AgentLens account, sign-in, an eligible active plan, and sufficient fetch credits.

Review your current allowance, operation costs, and plan details on the [AgentLens website](https://agentlensapi.io/) before fetching. A credit should not be assumed to equal one downloaded media file. Profile pagination and additional fetches may use credits separately.

Account registration, sign-in authorization, and plan management for this release use the website. Subscription checkout continues to Stripe after you review the plan there.

## Network access and data processing

The plugin sends the post or creator URL you enter, required installation/client identifiers, and sign-in authorization data to **AgentLens API at `agentlensapi.io`** for sign-in, link parsing, and media fetching. The service returns media details and download information. After import, the plugin reports per-item import results to the service.

Previews and media downloads need network access. Selected files may be downloaded through local temporary files before being imported into Eagle. Website authentication and subscription checkout use their respective external services, including Google sign-in and Stripe where selected.

Only retrieve and save content you own or have permission to use. Public availability does not grant redistribution rights.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| A URL cannot be parsed | Check that it is complete, supported, and appropriate for the selected post or profile workflow. Try a public source that is still available. |
| Account access is unavailable | Complete sign-in, return to Eagle, and review your plan and credits. |
| Parsing works but some files fail to import | Check your connection, disk space, and destination. Review which files saved before retrying. A fresh parse may be needed if download links expired. |
| Metadata is incomplete | Some sources do not return every field. Check the original post for missing context. |

## Support

Use this repository's **Issues** tab to report problems. Include the plugin version, Eagle version, operating system, steps to reproduce, and the displayed error. Share a public example URL when possible.

Remove passwords, tokens, private content, and payment information from reports and screenshots.

AgentLens Social Importer is a third-party plugin for Eagle. It is not developed or endorsed by Eagle or the supported social platforms.
