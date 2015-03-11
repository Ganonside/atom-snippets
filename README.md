# atom-snippets

This repo contains all the snippets I have created in atom.

The following lists show the snippet names followed by their prefixes.

## For `.js` Files

#### `log` -> console.log
```
console.log(${2:`${1:log}`});$3
```

#### `error` -> console.error
```
console.error(${3:`${2:Error: }$1`});$4
```

#### `req` -> require
```
var $1 = require(\'${2:./}$3\');
```

#### `/**` -> multiline comment
```
/**
 * ${1:Your comment here}
 */
```

#### `todo` -> todo
```
// TODO: $1
```

#### `class6` -> es6 class
```
class $1 {

  constructor(${2:params}) {
    let fields = {
      $3
    } = ${2:params};
  }
}

module.exports = $1;
```

#### `class6doc` -> es6 class w/ jsdoc
```
/**
 * The description of this class
 *
 * @class
 */
class $1 {

  constructor(${2:params}) {
    let fields = {
      $3
    } = ${2:params};
  }
}

module.exports = $1;
```

#### `sclass6` -> es6 static class
```
class ${1:className} {

  static ${2:someStaticMethod}(${3:params}) {
    $4
  }
  $5
}

module.exports = ${1:className};
```

#### `m` -> method
```
$1($2) {
  $3
}
```

#### `sm` -> static method
```
static $1($2) {
  $3
}
```

#### `mdoc` -> method w/ jsdoc
```
/**
 * ${4:description}
 *
 * @param {${3:type}} $2
 */
$1($2) {
  $5
}
```

#### `smdoc` -> static method w/ doc
```
/**
 * ${4:description}
 *
 * @param {${3:type}} $2
 */
static $1($2) {
  $5
}
```

#### `get` -> getter
```
get $1() {
  return $2;
}
$3
```

#### `set` -> setter
```
set $1($2) {
  let temp = this.$2
  this.$2 = $2;

  return temp;
}
$3
```

#### `prom6` -> es6 promise
```
$1($2)
  .then(res => {
    $3
  }).catch(err => {
    $4
  });
```

#### `newprom6` -> new es6 promise
```
new Promise((resolve, reject) => {
  $1
});
```

#### `switch` -> switch statement
```
switch($1) {
  case $2:
    $3
    break;
  $4
}
```

#### `case` -> case statement
```
case $1:
  $2
  ${3:break;}
$4
```

#### `tc` -> try catch
```
try {
  $1
}
catch (err) {
  $2
}$3
```

#### `tcf` -> try catch finally
```
try {
  $1
}
catch (err) {
  $2
}
finally {
  $3
}$4
```



## For `.jsx` Files

#### `rc6` -> React create class es6
```
var React = require('react');

var $1 = React.createClass({

  render() {
    $3

    return (
      ${2:<div />}
    );
  }

});

module.exports = $1;
```

#### `rel` -> React element
```
<$1 $2>
  $3
</$1>$4
```

#### `relc` -> self-closing React
```
<$1 $2/>$3
```
