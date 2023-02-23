## Description

🧰 Frontend tools to write plugin development easier for FiveM.

## Installation

Using `npm`:

```
npm install fivem-utils
```

Using `yarn`:

```
yarn add fivem-utils
```

## Example Uses

You can use the examples in the subsection below to use the tools.

## isEnvBrowser

- Checks whether the development environment is a browser.

```javascript
isEnvBrowser(): boolean;
```

- Usage

```javascript
// import

const browser = isEnvBrowser();

console.log(browser); // returns true if the page developed is open in the browser.
```

## useNuiEvent

- Allows you to listen to nui callbacks.

```javascript
useNuiEvent(handler: (data: unknown) => void): void;
```

- Usage

```javascript
// import

useNuiEvent((event) => {
  console.log(event.data); // prints the event data.
});
```

## fetchNui

- Allows you to send requests to the client side.

```javascript
fetchNui(eventName: string, data: object): any;
```

- Usage

```javascript
// import

fetchNui("test", {
  name: "Mark Edward",
})
  .then((data) => {
    console.log(data); // prints if a return was provided by the game.
  })
  .catch((error) => {
    console.log(error);
  });
```

## debugData

- Simulates sending a callback by the client.

```javascript
debugData(data: object, delayTime: number): void;
```

- Usage

```javascript
// import

debugData(
  {
    action: "test",
    data: {
      name: "Mark Edward",
    },
  },
  500
);
```

## Discord Server

<a href="https://discord.gg/CCExrpU"><img src="https://invidget.switchblade.xyz/765378158043332618"/></a>

## License

[MIT](https://choosealicense.com/licenses/mit/)
