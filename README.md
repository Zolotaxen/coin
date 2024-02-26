class Coin:
    def __init__(self, value):
        self.value = value

    def __str__(self):
        return f"Coin: {self.value}"

class Wallet:
    def __init__(self):
        self.coins = []

    def add_coin(self, coin):
        self.coins.append(coin)

    def total_value(self):
        return sum(coin.value for coin in self.coins)

# Пример использования классов Coin и Wallet
coin1 = Coin(1)
coin2 = Coin(5)

wallet = Wallet()
wallet.add_coin(coin1)
wallet.add_coin(coin2)

print("Total value in wallet:", wallet.total_value())
