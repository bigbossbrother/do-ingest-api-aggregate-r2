# do-ingest-api-aggregate-r2

![GitHub Repo stars](https://img.shields.io/github/stars/bigbossbrother/do-ingest-api-aggregate-r2?style=social) ![GitHub forks](https://img.shields.io/github/forks/bigbossbrother/do-ingest-api-aggregate-r2?style=social) ![GitHub issues](https://img.shields.io/github/issues/bigbossbrother/do-ingest-api-aggregate-r2)

## Overview

Welcome to the **do-ingest-api-aggregate-r2** repository! This project aims to aggregate hundreds of thousands of files using a Durable Object, efficiently streaming them out to R2. It is designed to help developers and teams overcome limitations often encountered in file handling and data management.

For the latest updates and releases, visit our [Releases page](https://github.com/bigbossbrother/do-ingest-api-aggregate-r2/releases).

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Durable Object Integration**: Leverage Durable Objects for reliable file aggregation.
- **High Capacity**: Handle hundreds of thousands of files seamlessly.
- **Efficient Streaming**: Stream files directly to R2, ensuring quick access and retrieval.
- **Limitations Circumvention**: Designed to bypass common limitations in file handling.

## Installation

To get started with **do-ingest-api-aggregate-r2**, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/bigbossbrother/do-ingest-api-aggregate-r2.git
   ```
2. Navigate to the project directory:
   ```bash
   cd do-ingest-api-aggregate-r2
   ```
3. Install the necessary dependencies:
   ```bash
   npm install
   ```

4. Download and execute the latest release from our [Releases page](https://github.com/bigbossbrother/do-ingest-api-aggregate-r2/releases).

## Usage

After installation, you can start using the API. Here’s a simple example to get you started:

```javascript
const { IngestAPI } = require('do-ingest-api-aggregate-r2');

const api = new IngestAPI();

api.aggregateFiles('/path/to/your/files')
   .then(response => {
       console.log('Files aggregated successfully:', response);
   })
   .catch(error => {
       console.error('Error aggregating files:', error);
   });
```

### Configuration

You can configure the API settings through a configuration file. Create a `config.json` file in the root directory with the following structure:

```json
{
    "r2Bucket": "your-bucket-name",
    "durableObjectID": "your-durable-object-id"
}
```

## API Reference

### IngestAPI

The main class for interacting with the API.

#### Methods

- **aggregateFiles(path: string)**: Aggregates files from the specified path.
  - **Parameters**:
    - `path`: The directory containing files to aggregate.
  - **Returns**: A promise that resolves with the aggregation result.

- **streamToR2()**: Streams the aggregated files to R2.
  - **Returns**: A promise that resolves when the streaming is complete.

## Contributing

We welcome contributions! If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m 'Add your feature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature/YourFeature
   ```
5. Create a pull request.

Please ensure your code adheres to our coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

If you have any questions or issues, feel free to open an issue on GitHub. For the latest updates, check our [Releases page](https://github.com/bigbossbrother/do-ingest-api-aggregate-r2/releases).

Thank you for your interest in **do-ingest-api-aggregate-r2**! We hope this project helps you efficiently manage your files and data.