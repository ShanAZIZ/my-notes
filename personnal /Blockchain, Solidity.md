# Blockchain, Solidity 

```
// SPDX-Licence-Identifier: MIT

pragma solidity ^0.6.0;

contract SimpleStorage {

    // this will get initialized to 0!
    uint256 favoriteNumber;
    bool favoriteBool;
    bool favoriteBool1;

    struct People {
        uint256 favoriteNumber;
        string name;
    }

    People[] public people; // Array
    mapping(string => uint256) public nameToFavoriteNumber;

    // instanciate a People person
    People public person = People({favoriteNumber: 2, name: "Patrick" });

    function store(uint256 _favoriteNumber) public {
        favoriteNumber = _favoriteNumber;
    }

    // view, pure
    function retrieve() public view returns(uint256) {
        return favoriteNumber;
    }

    function addPerson(string memory _name, uint256 _favoriteNumber) public {
        people.push(People(_favoriteNumber, _name));
        nameToFavoriteNumber[_name] = _favoriteNumber;
    }

}
```
