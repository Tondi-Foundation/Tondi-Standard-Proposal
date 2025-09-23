# Tondi OP CODE Summary Document

## Overview

This document is based on the opcode implementation in the Tondi client code, summarizing all available operation codes (OP CODE) in the current Tondi blockchain system. Tondi's script system is based on Bitcoin-like script language but with extensions and optimizations.

## Core Constants

- **Maximum Script Public Key Version**: 0
- **Maximum Stack Size**: 244
- **Maximum Script Size**: 10,000 bytes
- **Maximum Script Element Size**: 520 bytes
- **Maximum Operations Per Script**: 201
- **Maximum Public Keys Per Multisig**: 20

## OP CODE Categories

### 1. Data Push Opcodes (0x00-0x4e)

#### Empty Data Push
- **OpFalse (0x00)**: Push empty array onto stack

#### Fixed Length Data Push (OpData1-OpData75)
- **OpData1 (0x01)** - **OpData75 (0x4b)**: Push 1-75 bytes of data onto stack

#### Variable Length Data Push
- **OpPushData1 (0x4c)**: Read next byte as length N, push next N bytes of data
- **OpPushData2 (0x4d)**: Read next 2 bytes as length N, push next N bytes of data  
- **OpPushData4 (0x4e)**: Read next 4 bytes as length N, push next N bytes of data

#### Number Push
- **Op1Negate (0x4f)**: Push -1 onto stack
- **OpSuccess (0x50)**: Success operation (reserved)
- **OpTrue/Op1 (0x51)**: Push 1 onto stack
- **Op2 (0x52)** - **Op16 (0x60)**: Push 2-16 onto stack

### 2. Control Flow Opcodes (0x61-0x68)

- **OpNop (0x61)**: No operation
- **OpVer (0x62)**: Reserved opcode
- **OpIf (0x63)**: Execute next statements if top stack element is non-zero
- **OpNotIf (0x64)**: Execute next statements if top stack element is zero
- **OpVerIf (0x65)**: Reserved opcode
- **OpVerNotIf (0x66)**: Reserved opcode
- **OpElse (0x67)**: Execute else branch
- **OpEndIf (0x68)**: End if/else block

### 3. Stack Opcodes (0x69-0x7d)

#### Verification and Return
- **OpVerify (0x69)**: Verify top stack element, pop if non-zero
- **OpReturn (0x6a)**: Immediately fail script

#### Alternative Stack Operations
- **OpToAltStack (0x6b)**: Pop element from main stack to alt stack
- **OpFromAltStack (0x6c)**: Pop element from alt stack to main stack

#### Stack Operations
- **Op2Drop (0x6d)**: Drop top two stack elements
- **Op2Dup (0x6e)**: Duplicate top two stack elements
- **Op3Dup (0x6f)**: Duplicate top three stack elements
- **Op2Over (0x70)**: Copy top two stack elements to front
- **Op2Rot (0x71)**: Move top two stack elements to front
- **Op2Swap (0x72)**: Swap top two pairs of elements
- **OpIfDup (0x73)**: Duplicate top stack element unless it is zero
- **OpDepth (0x74)**: Push current stack depth
- **OpDrop (0x75)**: Drop top stack element
- **OpDup (0x76)**: Duplicate top stack element
- **OpNip (0x77)**: Drop second-to-top stack element
- **OpOver (0x78)**: Copy second-to-top stack element
- **OpPick (0x79)**: Copy Nth stack element to top
- **OpRoll (0x7a)**: Move Nth stack element to top
- **OpRot (0x7b)**: Rotate top three stack elements
- **OpSwap (0x7c)**: Swap top two stack elements
- **OpTuck (0x7d)**: Copy top stack element to second position

### 4. String Opcodes (0x7e-0x82) - Disabled

- **OpCat (0x7e)**: Concatenate two arrays (disabled)
- **OpSubStr (0x7f)**: Return section of an array (disabled)
- **OpLeft (0x80)**: Keep only bytes left of specified point in array (disabled)
- **OpRight (0x81)**: Keep only bytes right of specified point in array (disabled)
- **OpSize (0x82)**: Push length of top stack element

### 5. Bitwise Opcodes (0x83-0x86) - Disabled

- **OpInvert (0x83)**: Flip all bits in input (disabled)
- **OpAnd (0x84)**: Boolean AND between each bit in inputs (disabled)
- **OpOr (0x85)**: Boolean OR between each bit in inputs (disabled)
- **OpXor (0x86)**: Boolean XOR between each bit in inputs (disabled)

### 6. Comparison Opcodes (0x87-0x88)

- **OpEqual (0x87)**: Push 1 if inputs are exactly equal, 0 otherwise
- **OpEqualVerify (0x88)**: Return success if inputs are exactly equal, failure otherwise

### 7. Reserved Opcodes (0x89-0x8a)

- **OpSuccess1 (0x89)**: Reserved opcode (always succeeds)
- **OpSuccess2 (0x8a)**: Reserved opcode (always succeeds)

### 8. Arithmetic Opcodes (0x8b-0xa5)

#### Unary Operations
- **Op1Add (0x8b)**: Add 1 to top stack element
- **Op1Sub (0x8c)**: Subtract 1 from top stack element
- **OpNegate (0x8f)**: Multiply top stack element by -1
- **OpAbs (0x90)**: Absolute value of top stack element
- **OpNot (0x91)**: Map 0 to 1, everything else to 0
- **Op0NotEqual (0x92)**: Map 0 to 0, everything else to 1

#### Binary Operations
- **OpAdd (0x93)**: Pop two stack elements and push their sum
- **OpSub (0x94)**: Pop two stack elements and push second minus first
- **OpMul (0x95)**: Multiplication (disabled)
- **OpDiv (0x96)**: Division (disabled)
- **OpMod (0x97)**: Modulo (disabled)
- **OpLShift (0x98)**: Left shift (disabled)
- **OpRShift (0x99)**: Right shift (disabled)

#### Logical Operations
- **OpBoolAnd (0x9a)**: Pop two stack elements, push 1 if both non-zero, else 0
- **OpBoolOr (0x9b)**: Pop two stack elements, push 1 if either non-zero, else 0

#### Numeric Comparisons
- **OpNumEqual (0x9c)**: Pop two stack elements, push 1 if numerically equal, else 0
- **OpNumEqualVerify (0x9d)**: Pop two stack elements, return success if numerically equal, else failure
- **OpNumNotEqual (0x9e)**: Pop two stack elements, push 0 if numerically equal, else 1
- **OpLessThan (0x9f)**: Pop two elements, push 1 if second < first, else 0
- **OpGreaterThan (0xa0)**: Pop two elements, push 1 if second > first, else 0
- **OpLessThanOrEqual (0xa1)**: Pop two elements, push 1 if second <= first, else 0
- **OpGreaterThanOrEqual (0xa2)**: Pop two elements, push 1 if second >= first, else 0

#### Other Numeric Operations
- **OpMin (0xa3)**: Pop two elements, push smaller one
- **OpMax (0xa4)**: Pop two elements, push larger one
- **OpWithin (0xa5)**: Pop three elements, push 1 if first >= second and < third, else 0

### 9. Undefined Opcodes (0xa6-0xa7)

- **OpUnknown166 (0xa6)**: Undefined opcode
- **OpUnknown167 (0xa7)**: Undefined opcode

### 10. Cryptographic Opcodes (0xa8-0xaf)

- **OpSHA256 (0xa8)**: Pop top stack element and push its SHA256 hash
- **OpCheckMultiSigECDSA (0xa9)**: ECDSA multisig verification
- **OpBlake3 (0xaa)**: Pop top stack element and push its Blake3 hash
- **OpCheckSigECDSA (0xab)**: ECDSA signature verification
- **OpCheckSig (0xac)**: Schnorr signature verification, push 1/0 for success/failure
- **OpCheckSigVerify (0xad)**: Schnorr signature verification, return success/failure
- **OpCheckMultiSig (0xae)**: Schnorr multisig verification, push 1/0 for success/failure
- **OpCheckMultiSigVerify (0xaf)**: Schnorr multisig verification, return success/failure

### 11. Time Lock Opcodes (0xb0-0xb1)

- **OpCheckLockTimeVerify (0xb0)**: Check lock time verification
- **OpCheckSequenceVerify (0xb1)**: Check sequence verification

### 12. KIP-10 Transaction Introspection Opcodes (0xb2-0xc3)

These opcodes are only available when KIP-10 is enabled:

#### Transaction Level Opcodes
- **OpTxVersion (0xb2)**: Reserved opcode
- **OpTxInputCount (0xb3)**: Get number of inputs
- **OpTxOutputCount (0xb4)**: Get number of outputs
- **OpTxLockTime (0xb5)**: Reserved opcode
- **OpTxSubnetId (0xb6)**: Reserved opcode
- **OpTxGas (0xb7)**: Reserved opcode
- **OpTxPayload (0xb8)**: Reserved opcode

#### Input Related Opcodes
- **OpTxInputIndex (0xb9)**: Get current input index
- **OpOutpointTxId (0xba)**: Reserved opcode
- **OpOutpointIndex (0xbb)**: Reserved opcode
- **OpTxInputScriptSig (0xbc)**: Reserved opcode
- **OpTxInputSeq (0xbd)**: Reserved opcode
- **OpTxInputAmount (0xbe)**: Get input amount
- **OpTxInputSpk (0xbf)**: Get input script public key
- **OpTxInputBlockDaaScore (0xc0)**: Reserved opcode
- **OpTxInputIsCoinbase (0xc1)**: Reserved opcode

#### Output Related Opcodes
- **OpTxOutputAmount (0xc2)**: Get output amount
- **OpTxOutputSpk (0xc3)**: Get output script public key

### 13. Undefined Opcodes (0xc4-0xf9)

- **OpUnknown196 (0xc4)** - **OpUnknown249 (0xf9)**: Undefined opcodes

### 14. Special Opcodes (0xfa-0xff)

- **OpSmallInteger (0xfa)**: Reserved opcode
- **OpPubKeys (0xfb)**: Reserved opcode
- **OpUnknown252 (0xfc)**: Reserved opcode
- **OpPubKeyHash (0xfd)**: Reserved opcode
- **OpPubKey (0xfe)**: Reserved opcode
- **OpInvalidOpCode (0xff)**: Invalid opcode

## Important Features

### KIP-10 Support
KIP-10 introduces the following important features:
1. **8-byte Integer Arithmetic**: Support for larger numerical operations
2. **Transaction Introspection Opcodes**: Allow scripts to access transaction data
3. **Runtime Signature Operation Counting**: Accurate calculation of actually executed signature operations

### Signature Support
Tondi supports two signature algorithms:
- **Schnorr Signatures**: Default signature algorithm, 32-byte public keys
- **ECDSA Signatures**: Compatibility signature algorithm, 33-byte public keys

### Hash Algorithms
- **SHA256**: Standard SHA256 hash
- **Blake3**: High-performance hash algorithm (replaces Blake2b)

### Disabled Opcodes
The following opcodes are disabled for enhanced security:
- String operations: OpCat, OpSubStr, OpLeft, OpRight
- Bitwise operations: OpInvert, OpAnd, OpOr, OpXor
- Arithmetic operations: Op2Mul, Op2Div, OpMul, OpDiv, OpMod, OpLShift, OpRShift

## Usage Examples

### Basic P2PKH Script
```
<signature> <pubkey> OP_DUP OP_HASH160 <pubkeyhash> OP_EQUALVERIFY OP_CHECKSIG
```

### Multisig Script
```
<signature1> <signature2> <pubkey1> <pubkey2> <pubkey3> 3 OP_CHECKMULTISIG
```

### KIP-10 Introspection Script Example
```
OP_TXINPUTCOUNT 2 OP_EQUAL OP_VERIFY
OP_TXOUTPUTCOUNT 1 OP_EQUAL OP_VERIFY
```

## Summary

Tondi's OP CODE system is based on Bitcoin script language but with important extensions and optimizations:

1. **Enhanced Security**: Disabled potentially dangerous string and bitwise operation opcodes
2. **Performance Optimization**: Uses Blake3 instead of Blake2b, supports Schnorr signatures
3. **Feature Extension**: KIP-10 introduces transaction introspection capabilities, supporting more complex smart contracts
4. **Compatibility**: Maintains compatibility with Bitcoin scripts while adding Tondi-specific features

This OP CODE system provides Tondi blockchain with powerful and secure script execution capabilities, supporting everything from simple payments to complex smart contract applications.
