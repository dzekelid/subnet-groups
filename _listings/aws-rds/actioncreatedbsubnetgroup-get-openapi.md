---
swagger: "2.0"
x-collection-name: AWS RDS
x-complete: 0
info:
  title: Amazon RDS API Create D B Subnet Group
  version: 1.0.0
  description: Creates a new DB subnet group.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateDBSubnetGroup:
    get:
      summary: Create D B Subnet Group
      description: Creates a new DB subnet group.
      operationId: createdbsubnetgroup
      x-api-path-slug: actioncreatedbsubnetgroup-get
      parameters:
      - in: query
        name: DBSubnetGroupDescription
        description: The description for the DB subnet group
        type: string
      - in: query
        name: DBSubnetGroupName
        description: The name for the DB subnet group
        type: string
      - in: query
        name: SubnetIds.SubnetIdentifier.N
        description: The EC2 Subnet IDs for the DB subnet group
        type: string
      - in: query
        name: Tags.Tag.N
        description: A list of tags
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subnet Groups
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---