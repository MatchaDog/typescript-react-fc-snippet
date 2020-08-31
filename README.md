### This is a snippets for react function component, it supports typescriptreact, even you can use it in javascript or typescript; its not good for react class function.

# Support file type

-   javascript(\*.js)
-   typescript(\*.ts)
-   javascriptreact(\*.jsx)
-   typescriptreact(\*.tsx)

# Usage

Type a prefix, then press `tab`;

```bash
clg # press tab!
# ------>
console.log(|)
```

# tips

-   `$*` means the step order for next 'tabs'
-   some snippets support typescript, You just need to add a `ts` prefix in front

# handbook

## for console

| prefix | result                  |
| ------ | ----------------------- |
| clg    | console.log(\$1);       |
| ctb    | console.table(\$1);     |
| cer    | console.error(\"\$1\"); |
| ctm    | console.time();         |
| ctme   | console.timeEnd();      |
| cte    | console.trace();        |
| cwn    | console.warn(\"\$1\");  |
| cat    | console.assert(\$1);    |
| ccl    | console.clear();        |
| cct    | console.count(\$1);     |
| cgp    | console.group(\$1);     |
| cge    | console.groupEnd();     |
| cio    | console.info(\"\$1\");  |
| cdr    | console.dir();          |

## for es5 and next

| prefix | result                                                                                                           |
| ------ | ---------------------------------------------------------------------------------------------------------------- |
| cmt    | /\*_ <br>\${1:yourComments}<br> _/                                                                               |
| cmtf   | /\*_ <br> _ @description: ${1:description}<br> * @param {${2:paramType}}<br> _ @return {\${3:returnType}}<br> _/ |
| cda    | const [${2:propertyName}] = \${1:array};                                                                         |
| cdo    | const {${2:propertyName}} = ${1:object};                                                                         |
| im     | import \"\${1:module}\";                                                                                         |
| imd    | import { ${2:destructuredModule} } from \"${1:module}\";                                                         |
| ima    | import \* as ${2:alias} from \"${1:module}\;"                                                                    |
| imda   | import { \* as ${2:alias} } from \"${1:module}\";                                                                |
| edm    | export default \${1:module};                                                                                     |
| ems    | export {\${1:module}};                                                                                           |
| idxn   | import ${2:moduleName} from \"${1:pathName}\";<br>export default \${3:moduleName};                               |

## for react

| prefix | result                                     |
| ------ | ------------------------------------------ |
| imr    | import React from \"react\";               |
| imrs   | import React, { useState } from \"react\"; |

## for react function component

### cfc

```javascript
import react from "react";
const ${1:componentName} = () => {
    return <div></div>;
};
export default ${2:componentName};
```

### cefc

```javascript
import react from "react";
export const ${1:componentName} = () => {
    return <div></div>;
};
```

## for typescript

### tsimr

```typescript
import React, { FC } from "react";
```

### tscfc

```typescript
import React, { FC } from 'react';
interface IProps {};
const ${1:componentName}:FC<IProps> = (props) => {
    return <div>${3}</div>;
};
export default ${2:componentName};
```

### tscfrc

```typescript
import React, { ForwardRefRenderFunction, useImperativeHandle } from "react";
interface IProps {};
interface IHandles {};
const ${1:componentName}:ForwardRefRenderFunction<IHandles, IProps> = (props, ref) => {
    useImperativeHandle(ref, () => ({
        ${3:handles}
    }), [${4:dependencies}]);
    return <div></div>;
};
export default ${2:componentName};
```
## for hooks

### useState

```javascript
const [${1:state}, ${2:setState}] = useState(${3:defaultValue});
```

### useReducer

```javascript
const [state, dispatch] = useReducer(${1:reducer}, ${2:defaultValue}, ${3:init});
```

### useContext

```javascript
const ${1:value} = useContext(${2:context});
```

### useRef

```javascript
const ${1:refName} = useRef(${3:defaultValue});
```

### useImperativeHandle

```javascript
useImperativeHandle(${1:refName}, () => ({
    ${2:handles}
}), [${3:dependencies}]);
```

### useEffect

```javascript
useEffect(() => {
    ${1:effect}
    return () => {
        ${2:clear effect}
    }
}, [${3:dependencies}];
```

### useLayoutEffect

```javascript
    useLayoutEffect(() => {
        ${1:effect}
        return () => {
            ${2:clear effect}
        }
    }, [${3:dependencies}];
```

### useCallback

```javascript
const ${1:functionName} = useCallback(() => {
    ${2:callback}
}, [${3:dependencies}]);
```

### useMemo

```javascript
const ${1:memoName} = useMemo(() => ${2:ReactNodeName}, [${3:dependencies}]);
```

### useDebugValue

```javascript
useDebugValue(${1:value});
```
