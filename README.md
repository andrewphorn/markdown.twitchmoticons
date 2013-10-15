# A Twitch.tv-style Emoticon Extension for Markdown

This extension adds the ability to easily use Twitch.tv-style emoticons.

## Usage

### Default settings

```python
import markdown
text = """I'm going to go get WR for WindWaker HD Kappa"""
html = markdown.markdown(text, ["twitchmoticons"])
print(html)
```

```html
<p>I'm going to go get WR for WindWaker HD <img src="http://static-cdn.jtvnw.net/jtv_user_pictures/chansub-global-emoticon-ddc6e3a8732cb50f-25x28.png" /></p>
```

### Custom settings

```python
import markdown
text = """I'm going to go get WR for WindWaker HD Kappa"""
html = markdown.markdown(text,
    extensions = ["twitchmoticons"],
    extension_configs = {"twitchmoticons": [
        ("EMOTICONS", {"WindWaker": "WindWaker.jpg" }),
        ("BASE_URL",  "http://static.example.com/"   )
    ]}
)
print(html)
```

```html
<p>I'm going to go get WR for <img src="http://static.example.com/WindWaker.jpg" /> HD Kappa</p>
```