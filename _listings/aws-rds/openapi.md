---
swagger: "2.0"
x-collection-name: AWS RDS
x-complete: 1
info:
  title: AWS RDS API
  version: 1.0.0
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
  /?Action=DeleteDBSubnetGroup:
    get:
      summary: Delete D B Subnet Group
      description: Deletes a DB subnet group.
      operationId: deletedbsubnetgroup
      x-api-path-slug: actiondeletedbsubnetgroup-get
      parameters:
      - in: query
        name: DBSubnetGroupName
        description: The name of the database subnet group to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subnet Groups
  /?Action=DescribeDBSubnetGroups:
    get:
      summary: Describe D B Subnet Groups
      description: Returns a list of DBSubnetGroup descriptions.
      operationId: describedbsubnetgroups
      x-api-path-slug: actiondescribedbsubnetgroups-get
      parameters:
      - in: query
        name: DBSubnetGroupName
        description: The name of the DB subnet group to return details for
        type: string
      - in: query
        name: Filters.Filter.N
        description: This parameter is not currently supported
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous DescribeDBSubnetGroups
          request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subnet Groups
  /?Action=ModifyDBSubnetGroup:
    get:
      summary: Modify D B Subnet Group
      description: Modifies an existing DB subnet group.
      operationId: modifydbsubnetgroup
      x-api-path-slug: actionmodifydbsubnetgroup-get
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
        description: The EC2 subnet IDs for the DB subnet group
        type: string
      responses:
        200:
          description: OK
      tags:
      - Subnet Groups
---