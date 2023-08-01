# SQLAlchemy Discussion Questions

## Part One - Reading the Documentation

Looking at Documentation is an important part of programming. You don't have to memorize anything, but you should get familiar with the types of information you can find in different docs. For this exercise, using the SQLAlchemy documentation [here](https://docs.sqlalchemy.org/en/20/orm/session_basics.html#querying), take a look at the following session methods:

1. `.query`
2. `.filter_by`
3. `.get`
4. `.all`
5. `.add`
6. `.delete`

With your partner(s), try your best to find the answers to the following questions about each method above:

1. What argument or arguments does the method take?
2. What does the method return?
3. What happens if none of the parameters match? (ie. What if you are trying to find a specific Tweet and it can't be found?)

## Part Two - Name that SQL!

Pretend that you have a `tweets` table with three columns - `id`, `message` and `user_id`. Given the code below, write what SQL statements will fire when the following methods are called.

```python
class Tweet(Base):

    id = Column(Integer(), primary_key=True)
    message = Column(String())
    user_id = Column(Integer())

```

1. `session.query(Tweet).all()`
2. `session.add(tweet)`
3. `session.get(Tweet, 2)`
4. `session.query(Tweet).filter_by(user_id=3)`
5. `session.delete(tweet)`
6. `session.add_all([tweet1, tweet2])`