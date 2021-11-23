### SHARING INFORMATION BETWEEN BLOCKS USING REACT CONTEXTS

This article begins with a simple question, how is it possible to share data betweeen blocks. 

To give a little context the Sony's development team had to connect two blocks.

![To connect blocks](/arquivos/to_connect_blocks.png)

For previous decisions these blocks were separated in different rows wich difficulted connecting the blocks.

We thought that to use react context was a good idea but here is where appears the question, how to do it?

The first issue, it is understand how react context work, it should have a provider wich to wrap the children and also it will keep the context values.

## STEPS 

It is important to know about react context if you do not know it, learn more about this in:

- [Official documentation](https://reactjs.org/docs/context.html#gatsby-focus-wrapper)
- [A Guide to React Context and useContext() Hook](https://dmitripavlutin.com/react-context-and-usecontext/)
### STEP ONE

We should create the next files into custom app: 

![files](/arquivos/files.png)

Each file has a special function, we will begin speaking of `context.tsx` file.

```tsx
import { createContext } from 'react'

const HeaderContext = createContext({})

export default HeaderContext
```

Here we simply create the context and export it.

Thereafter we are going to work with the file that contains all our logic which is `state.tsx`

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










