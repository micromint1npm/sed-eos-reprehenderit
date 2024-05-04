# sessionstate

> 

[![NPM](https://img.shields.io/npm/v/@micromint1npm/sed-eos-reprehenderit.svg)](https://www.npmjs.com/package/@micromint1npm/sed-eos-reprehenderit) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save sessionstate
```

## Description

This simple hook should make it easier to add JSON and string objects to the window sessionStorage variable using useState.

## Usage

```jsx
// string

import React, { useEffect } from 'react'

import { useSessionState } from 'sessionstate'

const Example = () => {
  const [state, setState] = useSessionState("window.sessionStorage variable")
  useEffect(()=>{
    console.log("sessionStorage: " + window.sessionStorage["window.sessionStorage variable"])
    console.log("sessionState: " + state)
  }, [state])
  return (
    <div>      
      <p>{state}</p>
      <button onClick={()=>setState("Your value")}>Save value</button>
    </div>
  )
}

// JSON

import React, { useEffect } from 'react'

import { useSessionState } from 'sessionstate'

const Example = () => {
  const [state, setState] = useSessionState("window.sessionStorage variable")
  useEffect(()=>{
    console.log("sessionStorage: " + window.sessionStorage["window.sessionStorage variable"])
    console.log("sessionState: " + state)
  }, [state])
  return (
    <div>      
      <p>{state}</p>
      <button onClick={()=>setState([{"key1": "value1"}, {"key2": "value2"}])}>Save value</button>
    </div>
  )
}
```

## Feedback

If you find a bug or a flaw in the code, please email me: id_1.0@mail.ru.

Thanks you!

## License

MIT © [BEISER901](https://github.com/BEISER901)

---

This hook is created using [create-react-hook](https://github.com/hermanya/create-react-hook).
