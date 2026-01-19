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

GameSession -- Level
Level -- Wave
Wave -- Entity

Save -- GameSession
Save -- UserProfile

GameSession -- UserProfile

Shop -- UserProfile
Shop -- PowerUp

class Save {
    <<interface>>
    +loadSave()
    +saveCheckPoint(session: GameSession)
    +saveProfile(profile: UserProfile)
}

class GameSession {
    <<interface>>
    +getCurrentLevel()
    +nextLevel()
    +isGameOver()
}

class Level {
    <<interface>>
    +handleWaves()
    +getCurrentWave()
}

class Wave {
    <<interface>>
    +isWaveFinished()
}

class Entity {
    <<interface>>
    +getHealthPoints()
    +isAlive()
    +getCoordinates()
    +onCollision(otherEntity: Entity)
}

class Movable {
    <<interface>>
    +move()
}

class Shooter {
    <<interface>>
    +isAbleToShoot()
    +getFireRate()
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
