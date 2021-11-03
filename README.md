# Simple NFT Demo

## Intro
Duration: 0:02:00

This CodeLab shows a very simple implementation of NFT minting. The project does not include functionality for payment transactions or an UI, but the functionality can be tested through the Candid interface.<br><br>The project has the following functionality:

- Minting a NFT
- Transfer ownership
- Checking ownership of a NFT

Other features like payment, approvals and file uploads will be covered in future CodeLabs, as an extension of this project.

## Before you begin
Duration: 0:01:30

Before you start this tutorial, verify the following:
* You have an internet connection and access to a shell terminal on your local macOS or Linux computer.
* You have node.js installed if you want to include the default template files for front-end development in your project.
* You have downloaded and installed the DFINITY Canister SDK package as described in Download and install.
* You have installed the Visual Studio Code plugin for Motoko as described in Install the language editor plug-in if you are using Visual Studio Code as your IDE.
* You have stopped any Internet Computer network processes running on the local computer.

## NFT Metadata
Duration: 0:03:00
This project is *inspired* by the ERC721 token standard, and the standard's metadata format is being used. The functions are not strictly following the ERC721 standard.

**Metadata format:**
```
{
    "title": "Asset Metadata",
    "type": "object",
    "properties": {
        "name": {
            "type": "string",
            "description": "Identifies the asset to which this NFT represents"
        },
        "description": {
            "type": "string",
            "description": "Describes the asset to which this NFT represents"
        },
        "image": {
            "type": "string",
            "description": "A URI pointing to a resource with mime type image/* representing the asset to which this NFT represents. Consider making any images at a width between 320 and 1080 pixels and aspect ratio between 1.91:1 and 4:5 inclusive."
        }
    }
}
```

For more information about the ERC721 standard [see here](https://eips.ethereum.org/EIPS/eip-721)


## Before you begin

asd

## Create new project

asd


public func ownerOf(tokenId : TokenIndex) : async ?Owner 

dfx canister call ic_simple_nft ownerOf 20





public func transfer(from: Owner, to: Owner, tokenId: TokenIndex) : async TransferResponse 

dfx canister call ic_simple_nft transfer '(principal "j5zim-3qiww-r4e6e-upqsu-mvjps-ldjsb-mwygf-wrsvt-evbre-praau-lqe", principal "yh53e-3nnp7-zgyh3-oquli-lzacf-uidit-ibtjl-drtm4-h7uy4-b7pnl-pae", 20)'




public func mintNFT(to: Owner, name: Text, description: Text, tokenURI: Text) : async TokenIndex 

        //dfx canister call ic_simple_nft mintNFT '(principal "j5zim-3qiww-r4e6e-upqsu-mvjps-ldjsb-mwygf-wrsvt-evbre-praau-lqe", "My name", "my first NFT", "http://link-to-nft.com/img.jpg")'








