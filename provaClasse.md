classDiagram
Entity <|-- EnergyShield
Entity <|-- Bullet
Entity <|-- Enemy
Entity <|-- Player
Movable <|-- Enemy
Movable <|-- Player
Movable <|-- Bullet
Shooter <|-- Enemy
Shooter <|-- Player
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
    +onCollision(Entity: otherEntity)
}
class Shooter {
    <<interface>>
    +isAbleToShoot()
    +getFireRate()
}
class Movable {
    <<interface>>
    +move()
}
class EnergyShield {
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