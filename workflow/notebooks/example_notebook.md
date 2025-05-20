# Example Notebook

This is just a quick example showing how to use the template.


```python
import logging

logging.basicConfig(
	level=logging.INFO, format='%(asctime)s - %(levelname)s - %(message)s'
)

logger = logging.getLogger(__name__)
```

## Show tree of the DMP directories


```python
from damply import dirs as dmpdirs

print(dmpdirs)
```

    DamplyDirs<Structure: NESTED>
    Project Root: /Users/bhklab/TRASH/test-project-template
    CONFIG       : ├── config
    LOGS         : ├── logs
    METADATA     : ├── metadata
    NOTEBOOKS    : ├── workflow/notebooks
    PROCDATA     : ├── data/procdata
    RAWDATA      : ├── data/rawdata
    RESULTS      : ├── data/results
    SCRIPTS      : └── workflow/scripts


## Use the DMP `dmpdirs` object directly


```python
print(f'{dmpdirs.RAWDATA=} has {len(list(dmpdirs.RAWDATA.glob("*")))} files')
print(f'{dmpdirs.PROCDATA=} has {len(list(dmpdirs.PROCDATA.glob("*")))} files')
print(f'{dmpdirs.SCRIPTS=} has {len(list(dmpdirs.SCRIPTS.glob("*")))} files')
```

    dmpdirs.RAWDATA=PosixPath('/Users/bhklab/TRASH/test-project-template/data/rawdata') has 1 files
    dmpdirs.PROCDATA=PosixPath('/Users/bhklab/TRASH/test-project-template/data/procdata') has 1 files
    dmpdirs.SCRIPTS=PosixPath('/Users/bhklab/TRASH/test-project-template/workflow/scripts') has 2 files

