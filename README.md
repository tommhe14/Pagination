# discord.py-pagination

#### discord.py-pagination is a Python library to easily create embed paginators.

### Now updated [tommhe14] to store multiple messages and fork the corresponding one for display.

<img src="[https://cdn.soosbot.com/images/pagination-requirement.svg](https://cdn.discordapp.com/attachments/1222190576426815538/1232105864731824198/screamrobbo.jpg?ex=66283f81&is=6626ee01&hm=844dae95c7d83b0cc4c1376c229ee007aceafbd86c504f8348e14e6f62e175fd&)" alt="WARNING IMAGE NOT FOUND">

## Usage

### Quickstart
```python
import Paginator

# Create a list of embeds to paginate.
embeds = [discord.Embed(title="First embed"),
          discord.Embed(title="Second embed"),
          discord.Embed(title="Third embed")]

... # Inside a command.
await Paginator.Simple().start(ctx, pages=embeds)
```

### Advanced

##### To use custom buttons, pass in the corresponding argument when you initiate the paginator. **THESE ARE OPTIONAL**

```python
# These arguments override the default ones.

PreviousButton = discord.ui.Button(...)
NextButton = discord.ui.Button(...)
PageCounterStyle = discord.ButtonStyle(...) # Only accepts ButtonStyle instead of Button
InitialPage = 0 # Page to start the paginator on.
timeout = 42069 # Seconds to timeout. Default is 60
ephemeral = true # Defaults to false if not passed in.

await Paginator.Simple(
    PreviousButton=PreviousButton,
    NextButton=NextButton,
    PageCounterStyle=PageCounterStyle,
    InitialPage=InitialPage,
    timeout=timeout, ephemeral=ephemeral).start(ctx, pages=embeds)
```
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
