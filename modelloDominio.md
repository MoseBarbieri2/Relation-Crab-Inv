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

Save -- UserProfile
Shop -- UserProfile
Shop -- PowerUp

class Save {
    <<interface>>
    +loadSave()
    +saveCheckPoint(level: Level)
    +saveProfile(profile: UserProfile)
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

class UserProfile {
    <<interface>>
    +getCurrency()
    +hasPowerUp(powerUp: PowerUp)
}

class Shop {
    <<interface>>
    +purchase(profile: UserProfile, item: PowerUp)
}

class PowerUp {
    <<interface>>
    +getCost()
    +getLevel()
}