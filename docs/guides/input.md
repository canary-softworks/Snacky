# Respond to Input

Snacky allows you to respond to input on your Snackbars. The extent of this responsiveness is clicking the snackbar. To start, use the `BindToActivated` function. This will set up the snackbar to respond to input, and then run the provided function when clicked.

```lua
local New = Snacky.new({
    Name = "Example"
})

New:BindToActivation(function()
    print("Click!")
    if New.IsCurrentlyBroadcasting then
        New:CancelBroadcast()
    end
end)
```

If you would like your snackbar to stop responding from input, you can use the `UnbindFromActivated` function which will disable all properties regarding input.

```lua
New:UnbindFromActivated()
```