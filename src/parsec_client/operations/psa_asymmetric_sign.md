<!--
  -- Copyright (c) 2019, Arm Limited, All Rights Reserved
  -- SPDX-License-Identifier: Apache-2.0
  --
  -- Licensed under the Apache License, Version 2.0 (the "License"); you may
  -- not use this file except in compliance with the License.
  -- You may obtain a copy of the License at
  --
  -- http://www.apache.org/licenses/LICENSE-2.0
  --
  -- Unless required by applicable law or agreed to in writing, software
  -- distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
  -- WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  -- See the License for the specific language governing permissions and
  -- limitations under the License.
--->
# PsaAsymmetricSign

## Opcode: 4 (decimal), 0x0004 (hex)

## Summary

Sign a hash or short message with a private key.

Note that to perform a hash-and-sign signature algorithm, you must first calculate the hash of the data you want to sign. Then pass the resulting hash as the `hash` parameter to this function.

## Parameters

* **key_name** - Name of the key used for signing the hash.
* **hash** - Digest of the data to be signed. The digest must be in a raw binary format, with no padding or encoding unless the `RsaPkcs1v15Sign` algorithm is used, with no associated hash algorithm.

## Result values

* **signature** - Bytes forming up the requested signature

## Contract

[Protobuf](https://github.com/parallaxsecond/parsec-operations/blob/master/protobuf/asym_sign.proto)
