```python
from datetime import date
from damascus_university.ite_college import FourthYearStudent
from experience import two_years, one_year, decent
from creativity import alot

class Me(FourthYearStudent):
    """
    A passionated software engineer who likes to develop 2d games and large
    systems that needs to squeeze every cell of your brain to get it done,
    with some perfectionism I tweak code repeatedly trying to make it work
    perfectly and I always succeed. 
    """

    def __new__(cls):
        if not hasattr(cls, 'instance'):
            cls.instance = super(Me, cls).__new__(cls)
        return cls.instance
    
    def __init__(self):
        self.name = 'Salem Domani'
        self.birthdate = date(1999, 1, 4)

    @property
    def experience(self):
        return [
            two_years(of='.NET'),
            one_year(of='Django'),
            decent(of='React.js'),
        ]

    @property
    def creativity(self):
        return alot(limit=float('inf'))

    @property
    def hoppies(self):
        return [
            'Coding',
            'Game Development',
            'Drawing',
            'Learning',
        ]

    def contact_me(self):
        return 'salem.domani@gmail.com'

```