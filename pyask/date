"""Functions to ask date with specific format"""

import datetime

from .ask import ask
from functools import partial
from .utils import always_true, process

__all__ = ("date", "time", "time_and_date")

def date(question, aid="enter a date", **kwargs):
    """                                                             
using the ISO format.                                               
visit https://docs.python.org/3/library/datetime.html in the section
 classmethod date.fromisoformat(date_string) for a better understand
ing.                                                                
"""
    p_func = partial(process, datetime.date.fromisoformat, always_true)
    return ask(question, aid=aid, process_func=p_func, **kwargs)

def time(question, aid="enter the time in format %H:%M:&S", **kwargs):
    a = lambda x: (datetime.datetime.strptime(x, "%H:%M:%S").time())

    p_func = partial(process, a, always_true)
    return ask(question, aid=aid, process_func=p_func, **kwargs)

def time_and_date(question, aid="Enter the time and date in formar %%Y-%M-%D H:%M:%S", **kwargs):
    a = lambda x: (datetime.datetime.strptime(x, "%Y-%m-%d %H:%M:%S"))

    p_func = partial(process, a, always_true)
    return ask(question, aid=aid, process_func=p_func, **kwargs)
