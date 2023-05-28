# demo-rust-sqlite

https://github.com/diesel-rs/diesel

https://diesel.rs/guides/getting-started

## DIESEL

A safe, extensible ORM and Query Builder for Rust, supported databases:

- PostgreSQL
- MySQL
- SQLite

https://github.com/gluesql/gluesql

https://github.com/gluesql/gluesql-js

https://github.com/spacejam/sled

https://github.com/sqlparser-rs/sqlparser-rs

## sqlparser-rs example

To parse a simple `SELECT` statement:

```rust
use sqlparser::dialect::GenericDialect;
use sqlparser::parser::Parser;

let sql = "SELECT a, b, 123, myfunc(b) \
           FROM table_1 \
           WHERE a > b AND b < 100 \
           ORDER BY a DESC, b";

let dialect = GenericDialect {}; // or AnsiDialect, or your own dialect ...

let ast = Parser::parse_sql(&dialect, sql).unwrap();

println!("AST: {:?}", ast);
```

This outputs

```rust
AST: [Query(Query { ctes: [], body: Select(Select { distinct: false, projection: [UnnamedExpr(Identifier("a")), UnnamedExpr(Identifier("b")), UnnamedExpr(Value(Long(123))), UnnamedExpr(Function(Function { name: ObjectName(["myfunc"]), args: [Identifier("b")], over: None, distinct: false }))], from: [TableWithJoins { relation: Table { name: ObjectName(["table_1"]), alias: None, args: [], with_hints: [] }, joins: [] }], selection: Some(BinaryOp { left: BinaryOp { left: Identifier("a"), op: Gt, right: Identifier("b") }, op: And, right: BinaryOp { left: Identifier("b"), op: Lt, right: Value(Long(100)) } }), group_by: [], having: None }), order_by: [OrderByExpr { expr: Identifier("a"), asc: Some(false) }, OrderByExpr { expr: Identifier("b"), asc: None }], limit: None, offset: None, fetch: None })]
```

## wapm sqlite

https://webassembly.sh/?run-command=sqlite

https://wapm.io/sqlite/sqlite

https://github.com/wapm-packages/sqlite

https://github.com/wasienv/wasienv

https://docs.wasmer.io/ecosystem/wasienv/compile-c-c++-to-wasm-wasi

https://www.sqlitetutorial.net/sqlite-commands

wasmer --version

export http_proxy=http://127.0.0.1:1087;export https_proxy=http://127.0.0.1:1087;

wasmer self-update

wapm install sqlite

wapm run sqlite

wapm run sqlite foobar.db

- .help
- .quit .exit
- .open
- .database
- .tables
- .table '%es'
- .schema table_name



