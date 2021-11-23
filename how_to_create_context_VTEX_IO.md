# HOW TO CREATE CONTEXT AND SHARING INFORMATION BETWEEN BLOCKS

This article begin with a simple question, how is possible to share data betweeen blocks. 

To give a little context the Sony's development team had that to connect two blocks.

![To connect blocks](/arquivos/to_connect_blocks.png)

For previous decisions there blocks were separed in different rows wich difficulty to connect the blocks.

We thought that to use react context was a good idea but here is where appear the question, how do it?

The first, it is understand as react context work, it should have a provider wich to wrap the children and too it keep the context values.

## STEPS 

It is important to know about react context if you do not know it, you can review the next links:

- [Official documentation](https://reactjs.org/docs/context.html#gatsby-focus-wrapper)
- [A Guide to React Context and useContext() Hook](https://dmitripavlutin.com/react-context-and-usecontext/)
### STEP ONE

We should to create the next files into custom app: 

![files](/arquivos/files.png)

Each file has a special function, we will begin speaking of `context.tsx` file.

```tsx
import { createContext } from 'react'

const HeaderContext: any = createContext({})

export default HeaderContext
```

Here we simply create the context and export it.

Thereafter we are going to work with the file that contains all our logic wich it is `state.tsx`

```tsx
import Context from './context'
const HeaderState: FC = ({ children }) => {
  return (
    <Context.Provider>
      {children}
    </Context.Provider>
  )
}
```










