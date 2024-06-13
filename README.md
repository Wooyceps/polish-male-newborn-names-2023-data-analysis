
# Newborn Names Analysis

This project analyzes the popularity of newborn names in different regions. The data is based on the year 2023.

## Installation

To run this project, you need to have Python installed on your system. After cloning the repository, install the necessary Python packages using pip:

```bash
pip install -r requirements.txt
```

## Usage/Examples

The main script of this project is `main.ipynb`. It analyzes the popularity of a specific name across different regions. Here's a snippet from the script:

```python
name = 'MIKOŁAJ'
region_name_count = []
region_name_percent = []

for region in regional_data:
    region_name_count.append(region[region['IMIĘ_PIERWSZE'] == name]['LICZBA_WYSTĄPIEŃ'].sum())
    region_name_percent.append(region[region['IMIĘ_PIERWSZE'] == name]['%'].sum())

if sum(region_name_count) and sum(region_name_percent): 
    # Plotting code here...
else:
    print(f'Name {name} was not given to any newborn in 2023')
```

This script generates a bar chart showing the number and percentage of newborns named 'MIKOŁAJ' in each region in 2023.

## Contributing

Contributions are welcome. Please open an issue to discuss your idea or submit a Pull Request.

## License

This project is licensed under the MIT License.