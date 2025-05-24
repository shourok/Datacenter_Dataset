# Cloud Datacenter Simulation Dataset

This dataset contains synthetic data generated for simulating operations in a cloud datacenter environment. It includes:

- **3000 Nodes**: Representing physical or virtual servers.
- **3000 Node_VM**: Virtual machines assigned to nodes.
- **5000 Requests**: User or service requests directed to the datacenter.

## Dataset Structure

- `nodes.csv`- 3000 physical nodes with attributes like memory, processor, storage, and GPU.
- `node_vm.csv` - 3000 virtual machines mapped to nodes.
- `requests.csv` - 5000 simulated client requests (CPU/memory demands, duration, origin).

## Attributes Overview

### nodes.csv
| identity | labels | storage_type | processor_type | unique_id | memory | gpu_type | memory_type | storage | processor | gpu | available_processor | available_storage
| name | available_region | available_memory | available_gpu | elementId

|-----------|------|--------|-----------|---------|-----|--------|

### node_vm.csv
| identity | labels | node_vm_unique_id | estimation_run_time | cpu | health | request_unique_id | node_unique_id | start_date_time | status | ram | elementId
|-------|---------|------|------|------|-------------|

### requests.csv
| identity | labels | run_time | name | cpu | request_unique_id | id | ram | status | elementId

|------------|----------------|---------|---------|-------------|---------------|

## Usage
This dataset can be used for:
- Graph-based simulation in Neo4j.
- Cloud resource allocation testing.
- AI/ML-based scheduling and optimization models.

## Generator
Generated via a Python script using the Neo4j Graph Database API and `uuid`, `random`.

