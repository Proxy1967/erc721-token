# ERC721 Non-fungible token standard

A Non-fungible token (NFT) is a token used to identify something or someone in a unique way.

This token has many use cases, since it is providing everyone the information that someone is the owner of the NFT.

The non-fungible token (NFT) can represent collectible items, access keys, lottery tickets, numbered seats for events, visual and audio artworks, or even game items.

All NFTs have a `uint256` variable `tokenId`, so for any ERC-721 Contract, the pair `contract address` and `uint256 tokenId` must be globally unique.

A dapp (decentralized application) can have a "converter" that uses the unique `tokenId` as input and outputs an image or similar.

In order for a smart contract to be called an ERC-721 Non-fungible token it must implement the following methods and events.

**Methods**

```solidity
function balanceOf(address _owner) external view returns (uint256);
function ownerOf(uint256 _tokenId) external view returns (address);
function safeTransferFrom(address _from, address _to, uint256 _tokenId, bytes data) external payable;
function safeTransferFrom(address _from, address _to, uint256 _tokenId) external payable;
function transferFrom(address _from, address _to, uint256 _tokenId) external payable;
function approve(address _approved, uint256 _tokenId) external payable;
function setApprovalForAll(address _operator, bool _approved) external;
function getApproved(uint256 _tokenId) external view returns (address);
function isApprovedForAll(address _owner, address _operator) external view returns (bool);
```

**Events**

```solidity
event Transfer(address indexed _from, address indexed _to, uint256 indexed _tokenId);
event Approval(address indexed _owner, address indexed _approved, uint256 indexed _tokenId);
event ApprovalForAll(address indexed _owner, address indexed _operator, bool _approved);
```

**Sources used**

- [ethereum.org](https://ethereum.org/en/developers/docs/standards/tokens/erc-721/)
- [ERC-721: Non-Fungible Token Standard](https://eips.ethereum.org/EIPS/eip-721) - [github](https://github.com/ethereum/ercs/blob/master/ERCS/erc-721.md)
- [Openzeppelin implementation](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC721/ERC721.sol)
- [solmate implementation](https://github.com/transmissions11/solmate/blob/main/src/tokens/ERC721.sol)
