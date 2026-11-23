# Reddit discussion discovery

Find subreddits and threads worth joining for a product or piece of content, then hand over to the [Reddit guidance](../../self-media-platform-copywriting/references/reddit.md) in `self-media-platform-copywriting` to draft replies or posts. Read-only: do not log in, post or vote.

## Process

1. **Set keywords**: take 3 to 5 groups of English keywords from the product brief, covering the user's problem (such as `repurpose content multiple platforms`), the category (such as `AI agent social media`) and the ecosystem (such as `claude code skills`). Use the words people would search with, not the product name.
2. **Search for posts**: search posts from the last month for each keyword group, sorted by relevance. Record the subreddit, title, score, number of comments, posting time and link.
3. **Filter posts**: prefer posts where the original poster is asking a question, comments are still growing, the post is no more than two weeks old, and it is not locked or archived. Rank lower the posts whose comments are already flooded with similar products.
4. **Read the comments**: open the candidate posts, read the original post and the top comments, confirm there is still an angle nobody has answered, and record the real needs and objections in the comments.
5. **Read the rules**: read the rules of each candidate subreddit, and mark whether it bans AI-generated content, bans self-promotion or links, limits the share of self-promotion, or has a weekly thread for showing projects.
6. **Make the list**: for each candidate, give the post link, the subreddit, the rule verdict (reply with a link / reply without a link / do not join) and a suggested angle.

## Getting data through AIsa (optional)

When the environment variable `AISA_API_KEY` is set, public data can be fetched through the [AIsa](https://aisa.one) REST API (`https://api.aisa.one/apis/v1`). Add `X-AISA-Cost-Mode: quote` to each request first to get a price, tell the user the number of calls and the estimated cost, and run them only after the user agrees:

| Step | Endpoint | Main parameters |
|---|---|---|
| Search posts | `GET /reddit/search` | `query`, `filter=posts`, `sort=relevance`, `timeframe=month`, `trim=true` |
| Read comments | `GET /reddit/post/comments` | `url` (the post link), `trim=true` |
| Read rules | `GET /reddit/subreddit/details` | `subreddit` (case-sensitive) |

Measured in November 2026: each request cost about $0.0019. 5 keyword groups, 6 posts and 6 subreddits came to 17 requests, about $0.03 in total. The rules are in the `rules` field, as plain text.

Without a key, do the same steps in a browser with Reddit's own search and the subreddit sidebar, following [research-safety.md](research-safety.md).

## Notes

- The results only show where something is being discussed, not that promotion is welcome there. The rule verdict comes before popularity.
- Do not collect commenters' personal information; the list keeps only post links and summaries of public content.
