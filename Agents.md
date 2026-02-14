# 🤖 Agents Configuration for X Embed Functionality

## Agent: x-embed-manager

### Purpose
Automatically manage and update X (Twitter) embedded posts on the portfolio website.

### Capabilities
- Detect X/Twitter URLs in user messages
- Convert URLs to proper embed code
- Update HTML with new embedded tweets
- Maintain responsive design and styling
- Handle both individual tweets and timeline widgets

### Trigger Conditions
- User provides X/Twitter post URLs
- User mentions "embed", "Twitter", "X post", or "tweet"
- User requests to add social media content to website
- User says "update X posts" or similar

### Auto-Actions
1. **URL Detection**: Parse messages for X/Twitter URLs
2. **Embed Code Generation**: Create proper blockquote embed code
3. **HTML Update**: Replace placeholder content with actual tweets
4. **Style Validation**: Ensure CSS classes and responsive design
5. **Script Verification**: Confirm Twitter widgets script is loaded

### Response Template
```
🐦 X埋め込み機能を自動実行します

検出されたURL: [URL]
埋め込みタイプ: [個別ツイート/タイムライン]
更新場所: index.html

✅ 埋め込みコードを生成
✅ HTMLを更新
✅ デザインを調整

完了しました！ポートフォリオサイトでX投稿が表示されます。
```

### Configuration
- **Priority**: High
- **Auto-execute**: True
- **User-confirmation**: False (for URL detection)
- **Error-handling**: Fallback to manual instructions

### Files to Monitor
- `index.html` - Main portfolio page
- `x-embed-guide.md` - Usage documentation

### Dependencies
- Twitter Widgets script (https://platform.twitter.com/widgets.js)
- CSS classes: `.x-embed-container`, `.x-embed-item`, `.x-profile-widget`

---

## Agent: portfolio-optimizer

### Purpose
Continuously optimize and update the portfolio website based on new content and social media activity.

### Capabilities
- Monitor for portfolio content updates
- Suggest design improvements
- Update skills and project sections
- Integrate new social media content
- Maintain professional appearance

### Trigger Conditions
- New project completion mentioned
- Skills or certifications updated
- Social media content shared
- Portfolio design feedback received

### Auto-Actions
1. **Content Analysis**: Review new information for portfolio relevance
2. **Section Updates**: Add content to appropriate sections
3. **Design Consistency**: Ensure visual harmony across all elements
4. **SEO Optimization**: Update meta tags and descriptions
5. **Performance Check**: Validate responsive design and loading speed

---

## Integration Notes

### X Embed Workflow
1. User shares X URL → x-embed-manager activates
2. URL parsed and validated
3. Embed code generated automatically
4. HTML updated with new content
5. User notified of completion

### Best Practices
- Always preserve existing design patterns
- Maintain responsive grid layouts
- Use consistent styling with existing elements
- Test embed functionality after updates
- Provide clear user feedback on changes

### Error Handling
- Invalid URLs: Provide manual embed instructions
- Rate limits: Queue updates for later processing
- Embed failures: Fall back to simple link display
- CSS conflicts: Apply inline styles as needed