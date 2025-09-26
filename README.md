from abc import ABC, abstractmethod

class Figura(ABC):
    @abstractmethod
    def calcular_perimetro(self) -> float:
        pass

    @abstractmethod
    def calcular_area(self) -> float:
        pass

    @abstractmethod
    def obtener_nombre(self) -> str:
        pass

class Rectangulo(Figura):
    def __init__(self, base: float, altura: float):
        self.base = base
        self.altura = altura

    def calcular_perimetro(self) -> float:
        return 2 * (self.base + self.altura)

    def calcular_area(self) -> float:
        return self.base * self.altura

    def obtener_nombre(self) -> str:
        return "Rectángulo"

if __name__ == "__main__":
    r = Rectangulo(4, 7)
    print(r.obtener_nombre())
    print(f"Perímetro: {r.calcular_perimetro():.2f}")
    print(f"Área: {r.calcular_area():.2f}")
