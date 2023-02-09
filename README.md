# react-phonenumber-select

> Telephone number input React component. Made with jquery and select2.

[![NPM](https://img.shields.io/npm/v/@jeyserver/react-phonenumber-select.svg)](https://www.npmjs.com/@jeyserver/react-phonenumber-select) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

<img alt="React" src="https://img.shields.io/badge/react%20-%2320232a.svg?&style=for-the-badge&logo=react&logoColor=%2361DAFB"/> <img alt="TypeScript" src="https://img.shields.io/badge/typescript%20-%23007ACC.svg?&style=for-the-badge&logo=typescript&logoColor=white"/> <img alt="jQuery" src="https://img.shields.io/badge/jquery%20-%230769AD.svg?&style=for-the-badge&logo=jquery&logoColor=white"/>

## Install

```bash
npm i @jeyserver/react-phonenumber-select
```

## Usage

```jsx
import React, { useState } from 'react'
import { ReactPhonenumber } from 'reactphonenumber2'

const countries = [
  { code: 'IR', name: 'Iran', dialingCode: '98' },
  { code: 'AF', name: 'Afghanistan', dialingCode: '93' },
  { code: 'AL', name: 'Albania', dialingCode: '213' },
  { code: 'AS', name: 'American Samoa', dialingCode: '1684' }
]

const App = () => {
  const [phoneNumber, setphoneNumber] = useState<string>('')

  const changePhoneNumber = (phoneNumber: string, selected:any) => {
    console.log(JSON.stringify({
      phoneNumber, selected
    }, null, 2))
  }

  return (
    <div>
      <ReactPhonenumber
        onChange={changePhoneNumber}
        countries={countries}
        defaultCode="IR"
      />
    </div>
  )
}

export default App
```
