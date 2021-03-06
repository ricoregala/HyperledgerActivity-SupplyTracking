# Hyperledger Fabric Supply Chain Tracking Activity

## Development Environment:

### Operating System: Ubuntu Budgie 18.04.2 LTS

### Hyperledger Fabric Version : 1.4

### Go Version : 1.10.4

## PreRequisites:

1. Download github.com/ashtikuno/prerequisites.sh
2. Install Go https://golang.org/doc/install
   * To check the where the Go Path, Go Root, and Go Cache is located, run: `go env`
   * Based on the results of `go env`, export the Go path using  `export GOPATH=$HOME/go`
   * Based on the results of `go env`, extend the shell search path for Go using: `export PATH=$PATH:$GOPATH/bin`
3. Install curl: `sudo apt install curl -y`
4. `curl -sSL https://github.com/hyperledger/fabric/blob/release-1.4/scripts/bootstrap.sh | bash -s 1.4.0`
5. This will download the needed binaries and then put it into the bin folder of the download path.
6. Export the download path using: `export PATH=<path to download location>/bin:$PATH`
7. Run on command line:

<pre>
        go get github.com/golang/protobuf/proto
        go get github.com/hyperledger/fabric/common/attrmgr
        go get github.com/pkg/errors
        go get github.com/hyperledger/fabric/core/chaincode/lib/cid
</pre>

## Usage

1. `git clone https://github.com/ashtikuno/HyperledgerActivity-SupplyTracking.git`
<br/><br/>
Output:
<pre>fabric-samples/
  | ---- invoiceHyperledgerActivity-SupplyTracking/
                        | ---- Activity Instructions
                        | ---- basic-network
                        | ---- chaincode/supplytracking/go
                        | ---- supplytracking
</pre>

2. Change Directory to `/supplytracking` 
   * Install Dependencies by executing the following command: `npm install` or `npm i` 
   * Start the Fabric Network : `./startFabric.sh`
   * Enroll the Admin to the Network : `node enrollAmin.js`
   * Register the Users to the Network : `node registerUser.js`
3. Open a REST Client like [Insomnia](https://insomnia.rest/) or [Postman](https://www.getpostman.com/)
4. Test the End Point at : `http://localhost:3000`

## To Be Added:

<pre>
    ✔ Use of the Basic Network
    ✔ Query information from the block
    ✔ Update the block with new values
    ✖ Transfer of Assets
    ✖ n Number of USers
    ✖ User Interface
</pre>

## License

Copyright (c) 2019 Rico Regala
Licensed under the [Apache License 2.0](LICENSE)