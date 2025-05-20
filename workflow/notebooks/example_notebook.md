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
from damply import dirs

print(dirs)
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


## Use the DMP `dirs` object directly


```python
print(f'{dirs.RAWDATA=} has {len(list(dirs.RAWDATA.glob("*")))} files')
print(f'{dirs.PROCDATA=} has {len(list(dirs.PROCDATA.glob("*")))} files')
print(f'{dirs.SCRIPTS=} has {len(list(dirs.SCRIPTS.glob("*")))} files')
```

    dirs.RAWDATA=PosixPath('/Users/bhklab/TRASH/test-project-template/data/rawdata') has 1 files
    dirs.PROCDATA=PosixPath('/Users/bhklab/TRASH/test-project-template/data/procdata') has 1 files
    dirs.SCRIPTS=PosixPath('/Users/bhklab/TRASH/test-project-template/workflow/scripts') has 2 files

