                    +-------------------+
                    |       Product     |
                    +-------------------+
                    | - product_id (PK) |
                    | - name            |
                    | - manufacturer    |
                    +-------------------+
                            | 1
                            |
                            |
                    +------------------+
                    |     PetFood      |
                    +------------------+
                    | - food_id (PK)   |
                    | - weight         |
                    | - flavor         |
                    | - health_cond    |
                    +------------------+
                            | 1
                            |
                            |
                    +------------------+
                    |     PetToy       |
                    +------------------+
                    | - toy_id (PK)    |
                    | - material       |
                    | - durability     |
                    +------------------+
                            | 1
                            |
                            |
                    +-------------------+
                    |    PetApparel     |
                    +-------------------+
                    | - apparel_id (PK)|
                    | - color          |
                    | - size           |
                    | - care_instructions|
                    +-------------------+
                            |
                            |
                  +---------+----------+
                  |         |          |
                  |         |          |
                  |         |          |
          +------------+  +--------+  +------------+
          | Animal     |  | Manufacturer |  | Customer    |
          +------------+  +--------+  +------------+
          | - animal_id|  | - manu_id(PK)|  | - customer_id (PK) |
          | - name     |  | - name       |  | - name            |
          +------------+  +-------------+  | - email           |
                                            +-------------------+
                                                   |
                                                   |
                                                   |
                                           +-------------------+
                                           | Transaction       |
                                           +-------------------+
                                           | - transaction_id (PK) |
                                           | - customer_id (FK)   |
                                           | - date              |
                                           +-------------------+
                                                   |
                                                   |
                                                   |
                                           +------------------------+
                                           | Shipment               |
                                           +------------------------+
                                           | - shipment_id (PK)     |
                                           | - origin_location (FK) |
                                           | - destination_location (FK)|
                                           | - product_id (FK)      |
                                           | - quantity             |
                                           +------------------------+
