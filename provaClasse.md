classDiagram
Entity <|-- InanimateEntity
Entity <|-- LiveEntity
MovableObject <|-- Player
MovableObject <|-- Enemy
LiveEntity <|-- Enemy
LiveEntity <|-- Player
InanimateEntity <|-- Barrier
InanimateEntity <|-- Bullet
MovableObject <|-- Bullet
class Entity{
    <<inteface>>
}
class InanimateEntity {
    <<inteface>>
}
class LiveEntity {
    <<inteface>>
}
class Enemy {
    <<inteface>>
}
class Player{
    <<interface>>
}
class Barrier {
    <<inteface>>
}
class Bullet {
    <<inteface>>
}
class Level {
    <<inteface>>
    +spawnEnemies(enemies: Enemy)
}
class MovableObject {
    <<inteface>>
    +move()
}
