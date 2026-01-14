classDiagram
Entity <|-- Barrier
Entity <|-- Bullet
Entity <|-- Enemy
Entity <|-- Player
MovableEntity <|-- Enemy
MovableEntity <|-- Player
MovableEntity <|-- Bullet
ShootingEntity <|-- Enemy
ShootingEntity <|-- Player
Level -- Wave
Save -- Level
Entity -- Wave
class Save {
    <<interface>>
    +loadSave()
    +saveCheckPoint(level: Level)
    +saveProfile()
}
class Wave {
    <<interface>>
    +isWaveFinished()
}
class Level {
    <<interface>>
    +handleWaves()
    +getCurrentWave()
}
class Entity {
    <<interface>>
    +getHealthPoints()
    +isAlive()
    +getCoordinates()
}
class ShootingEntity {
    <<interface>>
    +canShoot()
    +setFireRate()
}
class MovableEntity {
    <<interface>>
    +move()
}
class Barrier {
    <<interface>>
}
class Enemy {
    <<interface>>
    +getEnemyType()
}
class Player {
    <<interface>>
}
class Bullet {
    <<interface>>
}