I = importlib
balances = Hash()
lockDates = Hash()
        
@export
def addAsset(contract: str, amt: float, y: int, m: int, d: int, h: int, ms: int):
    assert amt > 0, 'Cannot add a negative balance!'
    user = ctx.caller
    asset = I.import_module(contract)
    asset.transfer_from(amount=amt, to=ctx.this, main_account=user)
    lockDates[contract, user] = datetime.datetime(year=y, month=m, day=d, hour=h, minute=ms)
    balances[contract, user] += amt

@export
def removeAsset(contract: str, amt: float):
    assert amt > 0, 'Cannot withdraw negative balances!'
    user = ctx.caller
    d = lockDates[contract, user]
    assert now >= d, 'Cannot withdraw before locking period!'
    asset = I.import_module(contract)
    assert balances[contract, user] >= amt, 'Not enough balance to withdraw!'
    balances[contract, user] -= amt
    asset.transfer(amount=amt, to=user)
