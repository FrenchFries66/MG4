# MG4
## Devlog
Xiangyi Li, she/her

The FloatAnimation script makes the fish food move up and down over and over. It uses two member variables: _up, a bool that keeps track of the current direction, and _timer, a float that counts down the time left before the food changes direction.

In Start(), _timer is set to _switchSpeed, so the countdown starts at 3 seconds. Update() runs every frame. If _up is true, the food moves up with transform.Translate(0, _moveSpeed * Time.deltaTime, 0). If _up is false, it moves down with the negative speed. Since _up starts as false, the food moves down first.

Every frame, _timer decreases by Time.deltaTime. When _timer reaches 0, it is reset to _switchSpeed and _up is flipped to the opposite value with _up = !_up. This makes the food keep switching between up and down forever.

## Open-Source Assets
- [Quirky animal 3D models](https://assetstore.unity.com/packages/3d/characters/animals/quirky-series-free-animals-pack-178235)
- [City 3D models](https://assetstore.unity.com/packages/3d/environments/simplepoly-city-low-poly-assets-58899)
- [Bite sound effect](https://freesound.org/people/Jofae/sounds/353067/)