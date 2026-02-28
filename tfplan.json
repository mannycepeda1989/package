{
  "format_version": "1.2",
  "terraform_version": "1.13.5",
  "variables": {
    "aws_region": {
      "value": "eu-west-1"
    },
    "custom_tags_glue": {
      "value": {
        "ApplicationID": "2102",
        "ApplicationName": "DATA PLATFORM FOUNDATION",
        "Env": "sd",
        "Name": "glue"
      }
    },
    "custom_tags_lambda": {
      "value": {
        "ApplicationID": "2102",
        "ApplicationName": "DATA PLATFORM FOUNDATION",
        "Env": "sd",
        "Name": "lambda"
      }
    },
    "deny_exception_principals": {
      "value": [
        "arn:aws:iam::352383909183:user/eniaws-sa-ictd-400039_pscoped_01"
      ]
    },
    "department": {
      "value": "ict"
    },
    "env": {
      "value": "d"
    },
    "glue_crawler_iam_policies": {
      "value": [
        {
          "description": "Restricted Glue crawler related actions",
          "statements": [
            {
              "actions": [
                "glue:GetDatabase",
                "glue:GetTable",
                "glue:CreateTable",
                "glue:UpdateTable",
                "glue:GetSecurityConfiguration",
                "glue:GetConnection",
                "glue:StartCrawler",
                "glue:GetCrawler"
              ],
              "effect": "Allow",
              "resources": [],
              "sid": "AllowRestrictedGlueCrawlerActions"
            }
          ]
        }
      ]
    },
    "glue_crawlers": {
      "value": {
        "crawler_l0_raw": {
          "crawler_s3_target_path": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw/",
          "custom_tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd"
          },
          "database_key": "raw_db",
          "default_permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
          "iam_policies": [],
          "lineage_configuration": null,
          "schedule": null,
          "schema_change_policy": null,
          "scope": "bp1.0.0",
          "table_prefix": null
        }
      }
    },
    "glue_database_iam_policies": {
      "value": [
        {
          "description": "Restricted Glue catalog database related actions",
          "statements": [
            {
              "actions": [
                "glue:CreateDatabase",
                "glue:GetDatabase",
                "glue:UpdateDatabase",
                "glue:DeleteDatabase",
                "glue:GetTable",
                "glue:CreateTable",
                "glue:UpdateTable"
              ],
              "effect": "Allow",
              "resources": [],
              "sid": "AllowRestrictedGlueCatalogActions"
            }
          ]
        }
      ]
    },
    "glue_databases": {
      "value": {
        "raw_db": {
          "custom_tags": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "Env": "sd"
          },
          "description": "Glue database per i dati raw",
          "iam_policies": [
            {
              "name": "glue-db-policy",
              "statements": [
                {
                  "actions": [
                    "glue:GetDatabase",
                    "glue:GetTables"
                  ],
                  "effect": "Allow",
                  "resources": [
                    "arn:aws:glue:eu-west-1:899076912694:catalog",
                    "arn:aws:glue:eu-west-1:899076912694:database/raw_db",
                    "arn:aws:glue:eu-west-1:899076912694:table/raw_db/*"
                  ],
                  "sid": "GlueDatabaseRead"
                }
              ]
            }
          ],
          "scope": "raw",
          "tables": {
            "logs.ExtractionErrors": {
              "columns": [
                {
                  "name": "EntityName",
                  "type": "string"
                },
                {
                  "name": "InputRowsCount",
                  "type": "int"
                },
                {
                  "name": "ErrorRowsCount",
                  "type": "int"
                },
                {
                  "name": "SliceDate",
                  "type": "timestamp"
                },
                {
                  "name": "RunId",
                  "type": "string"
                },
                {
                  "name": "IsFullLoading",
                  "type": "string"
                }
              ],
              "database": "raw_db",
              "location_suffix": "/logs/ExtractionErrors/",
              "name": "extractionerrors",
              "parameters": {
                "format-version": "2",
                "table_type": "ICEBERG"
              },
              "storage": {
                "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
                "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
                "serde_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe",
                "serde_parameters": {
                  "serialization.format": "1"
                }
              },
              "table_type": "ICEBERG"
            },
            "logs.ExtractionErrorsDetail": {
              "columns": [
                {
                  "name": "EntityName",
                  "type": "string"
                },
                {
                  "name": "PK",
                  "type": "string"
                },
                {
                  "name": "Exceptions",
                  "type": "string"
                },
                {
                  "name": "LoadingSliceDate",
                  "type": "string"
                },
                {
                  "name": "AuditInputFile",
                  "type": "string"
                },
                {
                  "name": "AuditFileCreationDatetime",
                  "type": "timestamp"
                },
                {
                  "name": "AuditCurrentDatetime",
                  "type": "timestamp"
                },
                {
                  "name": "AuditSliceDate",
                  "type": "string"
                },
                {
                  "name": "AuditRunId",
                  "type": "string"
                },
                {
                  "name": "AuditIsFullLoading",
                  "type": "string"
                }
              ],
              "database": "raw_db",
              "location_suffix": "/logs/ExtractionErrorsDetail/",
              "name": "extractionerrorsdetail",
              "parameters": {
                "format-version": "2",
                "table_type": "ICEBERG"
              },
              "storage": {
                "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
                "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
                "serde_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe",
                "serde_parameters": {
                  "serialization.format": "1"
                }
              },
              "table_type": "ICEBERG"
            }
          }
        }
      }
    },
    "glue_iam_policies": {
      "value": [
        {
          "description": "Restricted Glue access for SSO role and IAM user",
          "statements": [
            {
              "actions": [
                "glue:GetJob",
                "glue:GetJobRun",
                "glue:StartJobRun",
                "glue:UpdateJob",
                "glue:GetTable",
                "glue:GetDatabase",
                "glue:GetPartition",
                "glue:BatchGetPartition",
                "glue:UpdateTable",
                "glue:UpdatePartition",
                "glue:BatchCreatePartition",
                "glue:BatchUpdatePartition",
                "glue:BatchStopJobRun"
              ],
              "effect": "Allow",
              "resources": [],
              "sid": "AllowRestrictedGlueActions"
            }
          ]
        }
      ]
    },
    "glue_version": {
      "value": "5.0"
    },
    "lambda_function_id": {
      "value": "bb-lambda-alfa-test"
    },
    "lambda_handler": {
      "value": "pdf_to_csv.handler.lambda_handler"
    },
    "lambda_memory_size": {
      "value": 256
    },
    "lambda_runtime": {
      "value": "python3.12"
    },
    "lineage_configuration": {
      "value": {
        "crawler_lineage_settings": "ENABLE"
      }
    },
    "network_exposure": {
      "value": "hybrid"
    },
    "number_of_workers": {
      "value": 2
    },
    "s3_bucket_artifacts": {
      "value": {
        "bucket_s3_access_logs_name": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
        "custom_tags": {
          "ApplicationID": "2102",
          "ApplicationName": "DATA PLATFORM FOUNDATION",
          "Env": "sd",
          "Name": "s3"
        },
        "iam_policies": [
          {
            "description": "Full S3 access for SSO role and IAM user",
            "statements": [
              {
                "actions": [
                  "s3:*"
                ],
                "effect": "Allow",
                "resources": [
                  "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts",
                  "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts/*"
                ],
                "sid": "AllowAllS3Actions"
              }
            ]
          }
        ]
      }
    },
    "schedule": {
      "value": "cron(0 12 * * ? *)"
    },
    "schema_change_policy": {
      "value": {
        "delete_behavior": "LOG",
        "update_behavior": "UPDATE_IN_DATABASE"
      }
    },
    "scope": {
      "value": "dpf-bp"
    },
    "script_location": {
      "value": ""
    },
    "subnet_ids": {
      "value": [
        "subnet-0bbf991ef124badcc",
        "subnet-0c4e308d22ad05ee7"
      ]
    },
    "table_prefix": {
      "value": "tbl_"
    },
    "vpc_id": {
      "value": "vpc-07dd8497864cf1073"
    },
    "worker_type": {
      "value": "G.1X"
    }
  },
  "planned_values": {
    "root_module": {
      "child_modules": [
        {
          "resources": [
            {
              "address": "module.blueprint.aws_glue_catalog_table.databases[\"raw_db.logs.ExtractionErrors\"]",
              "mode": "managed",
              "type": "aws_glue_catalog_table",
              "name": "databases",
              "index": "raw_db.logs.ExtractionErrors",
              "provider_name": "registry.terraform.io/hashicorp/aws",
              "schema_version": 0,
              "values": {
                "database_name": "raw_db",
                "description": null,
                "name": "extractionerrors",
                "open_table_format_input": [],
                "owner": null,
                "parameters": {
                  "format-version": "2",
                  "table_type": "ICEBERG"
                },
                "partition_keys": [],
                "region": "eu-west-1",
                "retention": null,
                "storage_descriptor": [
                  {
                    "additional_locations": null,
                    "bucket_columns": null,
                    "columns": [
                      {
                        "comment": null,
                        "name": "EntityName",
                        "parameters": null,
                        "type": "string"
                      },
                      {
                        "comment": null,
                        "name": "InputRowsCount",
                        "parameters": null,
                        "type": "int"
                      },
                      {
                        "comment": null,
                        "name": "ErrorRowsCount",
                        "parameters": null,
                        "type": "int"
                      },
                      {
                        "comment": null,
                        "name": "SliceDate",
                        "parameters": null,
                        "type": "timestamp"
                      },
                      {
                        "comment": null,
                        "name": "RunId",
                        "parameters": null,
                        "type": "string"
                      },
                      {
                        "comment": null,
                        "name": "IsFullLoading",
                        "parameters": null,
                        "type": "string"
                      }
                    ],
                    "compressed": null,
                    "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
                    "location": "s3://eniaws-s3-euwe1-ictd-899076912694-s3-access-logs/logs/ExtractionErrors/",
                    "number_of_buckets": null,
                    "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
                    "parameters": null,
                    "schema_reference": [],
                    "ser_de_info": [
                      {
                        "name": null,
                        "parameters": {
                          "serialization.format": "1"
                        },
                        "serialization_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe"
                      }
                    ],
                    "skewed_info": [],
                    "sort_columns": [],
                    "stored_as_sub_directories": null
                  }
                ],
                "table_type": "ICEBERG",
                "target_table": [],
                "view_expanded_text": null,
                "view_original_text": null
              },
              "sensitive_values": {
                "open_table_format_input": [],
                "parameters": {},
                "partition_index": [],
                "partition_keys": [],
                "storage_descriptor": [
                  {
                    "columns": [
                      {},
                      {},
                      {},
                      {},
                      {},
                      {}
                    ],
                    "schema_reference": [],
                    "ser_de_info": [
                      {
                        "parameters": {}
                      }
                    ],
                    "skewed_info": [],
                    "sort_columns": []
                  }
                ],
                "target_table": []
              }
            },
            {
              "address": "module.blueprint.aws_glue_catalog_table.databases[\"raw_db.logs.ExtractionErrorsDetail\"]",
              "mode": "managed",
              "type": "aws_glue_catalog_table",
              "name": "databases",
              "index": "raw_db.logs.ExtractionErrorsDetail",
              "provider_name": "registry.terraform.io/hashicorp/aws",
              "schema_version": 0,
              "values": {
                "database_name": "raw_db",
                "description": null,
                "name": "extractionerrorsdetail",
                "open_table_format_input": [],
                "owner": null,
                "parameters": {
                  "format-version": "2",
                  "table_type": "ICEBERG"
                },
                "partition_keys": [],
                "region": "eu-west-1",
                "retention": null,
                "storage_descriptor": [
                  {
                    "additional_locations": null,
                    "bucket_columns": null,
                    "columns": [
                      {
                        "comment": null,
                        "name": "EntityName",
                        "parameters": null,
                        "type": "string"
                      },
                      {
                        "comment": null,
                        "name": "PK",
                        "parameters": null,
                        "type": "string"
                      },
                      {
                        "comment": null,
                        "name": "Exceptions",
                        "parameters": null,
                        "type": "string"
                      },
                      {
                        "comment": null,
                        "name": "LoadingSliceDate",
                        "parameters": null,
                        "type": "string"
                      },
                      {
                        "comment": null,
                        "name": "AuditInputFile",
                        "parameters": null,
                        "type": "string"
                      },
                      {
                        "comment": null,
                        "name": "AuditFileCreationDatetime",
                        "parameters": null,
                        "type": "timestamp"
                      },
                      {
                        "comment": null,
                        "name": "AuditCurrentDatetime",
                        "parameters": null,
                        "type": "timestamp"
                      },
                      {
                        "comment": null,
                        "name": "AuditSliceDate",
                        "parameters": null,
                        "type": "string"
                      },
                      {
                        "comment": null,
                        "name": "AuditRunId",
                        "parameters": null,
                        "type": "string"
                      },
                      {
                        "comment": null,
                        "name": "AuditIsFullLoading",
                        "parameters": null,
                        "type": "string"
                      }
                    ],
                    "compressed": null,
                    "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
                    "location": "s3://eniaws-s3-euwe1-ictd-899076912694-s3-access-logs/logs/ExtractionErrorsDetail/",
                    "number_of_buckets": null,
                    "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
                    "parameters": null,
                    "schema_reference": [],
                    "ser_de_info": [
                      {
                        "name": null,
                        "parameters": {
                          "serialization.format": "1"
                        },
                        "serialization_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe"
                      }
                    ],
                    "skewed_info": [],
                    "sort_columns": [],
                    "stored_as_sub_directories": null
                  }
                ],
                "table_type": "ICEBERG",
                "target_table": [],
                "view_expanded_text": null,
                "view_original_text": null
              },
              "sensitive_values": {
                "open_table_format_input": [],
                "parameters": {},
                "partition_index": [],
                "partition_keys": [],
                "storage_descriptor": [
                  {
                    "columns": [
                      {},
                      {},
                      {},
                      {},
                      {},
                      {},
                      {},
                      {},
                      {},
                      {}
                    ],
                    "schema_reference": [],
                    "ser_de_info": [
                      {
                        "parameters": {}
                      }
                    ],
                    "skewed_info": [],
                    "sort_columns": []
                  }
                ],
                "target_table": []
              }
            }
          ],
          "address": "module.blueprint",
          "child_modules": [
            {
              "resources": [
                {
                  "address": "module.blueprint.module.glue_job.aws_glue_job.job",
                  "mode": "managed",
                  "type": "aws_glue_job",
                  "name": "job",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "command": [
                      {
                        "name": "glueetl",
                        "python_version": "3"
                      }
                    ],
                    "connections": null,
                    "default_arguments": {
                      "--continuous-log-logGroup": "/aws-glue/jobs",
                      "--enable-auto-scaling": "true",
                      "--enable-continuous-cloudwatch-log": "true",
                      "--enable-continuous-log-filter": "true",
                      "--enable-metrics": "",
                      "--job-language": "python"
                    },
                    "description": "Glue ETL job",
                    "execution_class": "STANDARD",
                    "execution_property": [
                      {
                        "max_concurrent_runs": 1
                      }
                    ],
                    "glue_version": "5.0",
                    "job_run_queuing_enabled": null,
                    "maintenance_window": null,
                    "max_retries": 1,
                    "name": "eniaws-glue-euwe1-ictd-899076912694-dpf-bp",
                    "non_overridable_arguments": null,
                    "notification_property": [
                      {
                        "notify_delay_after": 3
                      }
                    ],
                    "number_of_workers": 2,
                    "region": "eu-west-1",
                    "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp",
                    "source_control_details": [],
                    "tags": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "BuildingBlockName": "aws_glue",
                      "BuildingBlockVersion": "0.0.0",
                      "Env": "sd",
                      "Name": "glue"
                    },
                    "tags_all": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "BuildingBlockName": "aws_glue",
                      "BuildingBlockVersion": "0.0.0",
                      "Env": "sd",
                      "Name": "glue"
                    },
                    "timeout": 2880,
                    "worker_type": "G.1X"
                  },
                  "sensitive_values": {
                    "command": [
                      {}
                    ],
                    "default_arguments": {},
                    "execution_property": [
                      {}
                    ],
                    "notification_property": [
                      {}
                    ],
                    "source_control_details": [],
                    "tags": {},
                    "tags_all": {}
                  }
                },
                {
                  "address": "module.blueprint.module.glue_job.aws_glue_resource_policy.this",
                  "mode": "managed",
                  "type": "aws_glue_resource_policy",
                  "name": "this",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "enable_hybrid": "TRUE",
                    "region": "eu-west-1"
                  },
                  "sensitive_values": {},
                  "identity_schema_version": 0,
                  "identity": {
                    "account_id": null,
                    "region": null
                  }
                },
                {
                  "address": "module.blueprint.module.glue_job.aws_glue_security_configuration.this",
                  "mode": "managed",
                  "type": "aws_glue_security_configuration",
                  "name": "this",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "encryption_configuration": [
                      {
                        "cloudwatch_encryption": [
                          {
                            "cloudwatch_encryption_mode": "SSE-KMS",
                            "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/glue"
                          }
                        ],
                        "job_bookmarks_encryption": [
                          {
                            "job_bookmarks_encryption_mode": "CSE-KMS",
                            "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/glue"
                          }
                        ],
                        "s3_encryption": [
                          {
                            "kms_key_arn": null,
                            "s3_encryption_mode": "SSE-S3"
                          }
                        ]
                      }
                    ],
                    "name": "eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp",
                    "region": "eu-west-1"
                  },
                  "sensitive_values": {
                    "encryption_configuration": [
                      {
                        "cloudwatch_encryption": [
                          {}
                        ],
                        "job_bookmarks_encryption": [
                          {}
                        ],
                        "s3_encryption": [
                          {}
                        ]
                      }
                    ]
                  }
                },
                {
                  "address": "module.blueprint.module.glue_job.aws_iam_role.role",
                  "mode": "managed",
                  "type": "aws_iam_role",
                  "name": "role",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
                    "description": null,
                    "force_detach_policies": false,
                    "max_session_duration": 3600,
                    "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-dpf-bp",
                    "path": "/",
                    "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
                    "tags": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "Env": "sd",
                      "Name": "glue"
                    },
                    "tags_all": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "Env": "sd",
                      "Name": "glue"
                    }
                  },
                  "sensitive_values": {
                    "inline_policy": [],
                    "managed_policy_arns": [],
                    "tags": {},
                    "tags_all": {}
                  },
                  "identity_schema_version": 0,
                  "identity": {
                    "account_id": null,
                    "name": null
                  }
                },
                {
                  "address": "module.blueprint.module.glue_job.aws_iam_role_policy.glue_job_permissions",
                  "mode": "managed",
                  "type": "aws_iam_role_policy",
                  "name": "glue_job_permissions",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "name": "glue_job_permissions"
                  },
                  "sensitive_values": {},
                  "identity_schema_version": 0,
                  "identity": {
                    "account_id": null,
                    "name": null,
                    "role": null
                  }
                },
                {
                  "address": "module.blueprint.module.glue_job.data.aws_iam_policy_document.glue_job_combined_policy",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "glue_job_combined_policy",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": [
                      null,
                      "{\n  \"Version\": \"2012-10-17\",\n  \"Statement\": [\n    {\n      \"Sid\": \"AllowRestrictedGlueActions\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"glue:UpdateTable\",\n        \"glue:UpdatePartition\",\n        \"glue:UpdateJob\",\n        \"glue:StartJobRun\",\n        \"glue:GetTable\",\n        \"glue:GetPartition\",\n        \"glue:GetJobRun\",\n        \"glue:GetJob\",\n        \"glue:GetDatabase\",\n        \"glue:BatchUpdatePartition\",\n        \"glue:BatchStopJobRun\",\n        \"glue:BatchGetPartition\",\n        \"glue:BatchCreatePartition\"\n      ],\n      \"Resource\": \"arn:aws:glue:eu-west-1:899076912694:*\"\n    }\n  ]\n}"
                    ],
                    "statement": [],
                    "version": null
                  },
                  "sensitive_values": {
                    "source_policy_documents": [
                      false,
                      false
                    ],
                    "statement": []
                  }
                },
                {
                  "address": "module.blueprint.module.glue_job.data.aws_iam_policy_document.glue_job_policy",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "glue_job_policy",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": null,
                    "statement": [
                      {
                        "actions": [
                          "s3:DeleteObject",
                          "s3:GetBucketLocation",
                          "s3:GetObject",
                          "s3:ListBucket",
                          "s3:PutObject"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [],
                        "resources": [
                          null,
                          null
                        ],
                        "sid": "S3Access"
                      },
                      {
                        "actions": [
                          "logs:CreateLogGroup",
                          "logs:CreateLogStream",
                          "logs:DescribeLogGroups",
                          "logs:PutLogEvents"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [],
                        "resources": [
                          "arn:aws:logs:*:*:log-group:/aws-glue/*",
                          "arn:aws:logs:*:*:log-group:/aws-glue/*:*"
                        ],
                        "sid": "LogsAccess"
                      },
                      {
                        "actions": [
                          "cloudwatch:PutMetricData"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [],
                        "resources": [
                          "*"
                        ],
                        "sid": "CloudWatchMetrics"
                      },
                      {
                        "actions": [
                          "glue:BatchCreatePartition",
                          "glue:BatchGetPartition",
                          "glue:BatchStopJobRun",
                          "glue:BatchUpdatePartition",
                          "glue:GetDatabase",
                          "glue:GetJob",
                          "glue:GetJobRun",
                          "glue:GetPartition",
                          "glue:GetTable",
                          "glue:StartJobRun",
                          "glue:UpdateJob",
                          "glue:UpdatePartition",
                          "glue:UpdateTable"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [],
                        "resources": [
                          "arn:aws:glue:eu-west-1:899076912694:*"
                        ],
                        "sid": "GlueAccess"
                      },
                      {
                        "actions": [
                          "ec2:AttachNetworkInterface",
                          "ec2:CreateNetworkInterface",
                          "ec2:DeleteNetworkInterface",
                          "ec2:DetachNetworkInterface"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [],
                        "resources": [
                          "arn:aws:ec2:eu-west-1:899076912694:network-interface/*",
                          "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7",
                          "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4",
                          "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a",
                          "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb",
                          "arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f"
                        ],
                        "sid": "EC2Modify"
                      }
                    ],
                    "version": null
                  },
                  "sensitive_values": {
                    "statement": [
                      {
                        "actions": [
                          false,
                          false,
                          false,
                          false,
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [],
                        "resources": [
                          false,
                          false
                        ]
                      },
                      {
                        "actions": [
                          false,
                          false,
                          false,
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [],
                        "resources": [
                          false,
                          false
                        ]
                      },
                      {
                        "actions": [
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [],
                        "resources": [
                          false
                        ]
                      },
                      {
                        "actions": [
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [],
                        "resources": [
                          false
                        ]
                      },
                      {
                        "actions": [
                          false,
                          false,
                          false,
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [],
                        "resources": [
                          false,
                          false,
                          false,
                          false,
                          false,
                          false
                        ]
                      }
                    ]
                  }
                },
                {
                  "address": "module.blueprint.module.glue_job.data.aws_iam_policy_document.glue_resource_policy_doc",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "glue_resource_policy_doc",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": null,
                    "statement": [
                      {
                        "actions": [
                          "glue:*"
                        ],
                        "condition": [
                          {
                            "test": "StringEquals",
                            "values": [
                              "638883080465"
                            ],
                            "variable": "aws:VpceAccount"
                          }
                        ],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "*"
                            ],
                            "type": "*"
                          }
                        ],
                        "resources": [
                          "arn:aws:glue:eu-west-1:899076912694:*"
                        ],
                        "sid": "AllowActionsFromInsideVPC"
                      },
                      {
                        "actions": [
                          "glue:BatchGet*",
                          "glue:Get*",
                          "glue:List*"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                            ],
                            "type": "AWS"
                          }
                        ],
                        "resources": [
                          "arn:aws:glue:eu-west-1:899076912694:*"
                        ],
                        "sid": "AllowPrisma"
                      },
                      {
                        "actions": [
                          "glue:BatchGet*",
                          "glue:Get*",
                          "glue:List*"
                        ],
                        "condition": [
                          {
                            "test": "IpAddress",
                            "values": [
                              "10.68.98.160/27",
                              "10.68.98.128/27"
                            ],
                            "variable": "aws:VpcSourceIp"
                          },
                          {
                            "test": "StringEquals",
                            "values": [
                              "vpc-0fbd9e814ef60d4ac"
                            ],
                            "variable": "aws:SourceVpc"
                          }
                        ],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "*"
                            ],
                            "type": "*"
                          }
                        ],
                        "resources": [
                          "arn:aws:glue:eu-west-1:899076912694:*"
                        ],
                        "sid": "AllowPublicThroughF5"
                      },
                      {
                        "actions": [
                          "glue:*"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "arn:aws:iam::209923409268:role/AWSAFTExecution",
                              "arn:aws:iam::468861045281:role/AWSAFTExecution"
                            ],
                            "type": "AWS"
                          }
                        ],
                        "resources": [
                          "arn:aws:glue:eu-west-1:899076912694:*"
                        ],
                        "sid": "AllowAFTExecution"
                      },
                      {
                        "actions": null,
                        "condition": [
                          {
                            "test": "BoolIfExists",
                            "values": [
                              "false"
                            ],
                            "variable": "aws:PrincipalIsAWSService"
                          },
                          {
                            "test": "NotIpAddress",
                            "values": [
                              "10.68.98.160/27",
                              "10.68.98.128/27"
                            ],
                            "variable": "aws:VpcSourceIp"
                          },
                          {
                            "test": "StringNotEquals",
                            "variable": "aws:PrincipalArn"
                          },
                          {
                            "test": "StringNotEquals",
                            "values": [
                              "638883080465"
                            ],
                            "variable": "aws:VpceAccount"
                          }
                        ],
                        "effect": "Deny",
                        "not_actions": [
                          "glue:BatchGet*",
                          "glue:DeleteResourcePolicy",
                          "glue:Get*",
                          "glue:GetResourcePolicy",
                          "glue:List*",
                          "glue:PutResourcePolicy"
                        ],
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "*"
                            ],
                            "type": "AWS"
                          }
                        ],
                        "resources": [
                          "arn:aws:glue:eu-west-1:899076912694:*"
                        ],
                        "sid": "DenyNotPrincipals"
                      },
                      {
                        "actions": [
                          "glue:*"
                        ],
                        "condition": [
                          {
                            "test": "Bool",
                            "values": [
                              "false"
                            ],
                            "variable": "aws:SecureTransport"
                          }
                        ],
                        "effect": "Deny",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "*"
                            ],
                            "type": "*"
                          }
                        ],
                        "resources": [
                          "arn:aws:glue:eu-west-1:899076912694:*"
                        ],
                        "sid": "DenyNonHTTPS"
                      }
                    ],
                    "version": null
                  },
                  "sensitive_values": {
                    "statement": [
                      {
                        "actions": [
                          false
                        ],
                        "condition": [
                          {
                            "values": [
                              false
                            ]
                          }
                        ],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false
                        ]
                      },
                      {
                        "actions": [
                          false,
                          false,
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false
                        ]
                      },
                      {
                        "actions": [
                          false,
                          false,
                          false
                        ],
                        "condition": [
                          {
                            "values": [
                              false,
                              false
                            ]
                          },
                          {
                            "values": [
                              false
                            ]
                          }
                        ],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false
                        ]
                      },
                      {
                        "actions": [
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false,
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false
                        ]
                      },
                      {
                        "condition": [
                          {
                            "values": [
                              false
                            ]
                          },
                          {
                            "values": [
                              false,
                              false
                            ]
                          },
                          {
                            "values": []
                          },
                          {
                            "values": [
                              false
                            ]
                          }
                        ],
                        "not_actions": [
                          false,
                          false,
                          false,
                          false,
                          false,
                          false
                        ],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false
                        ]
                      },
                      {
                        "actions": [
                          false
                        ],
                        "condition": [
                          {
                            "values": [
                              false
                            ]
                          }
                        ],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false
                        ]
                      }
                    ]
                  }
                }
              ],
              "address": "module.blueprint.module.glue_job"
            },
            {
              "resources": [
                {
                  "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_glue_crawler.crawler",
                  "mode": "managed",
                  "type": "aws_glue_crawler",
                  "name": "crawler",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "catalog_target": [],
                    "classifiers": null,
                    "configuration": null,
                    "database_name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
                    "delta_target": [],
                    "description": null,
                    "dynamodb_target": [],
                    "hudi_target": [],
                    "iceberg_target": [],
                    "jdbc_target": [],
                    "lake_formation_configuration": [],
                    "lineage_configuration": [],
                    "mongodb_target": [],
                    "name": "eniaws-glue-crw-euwe1-ictd-899076912694-bp1.0.0",
                    "recrawl_policy": [],
                    "region": "eu-west-1",
                    "s3_target": [
                      {
                        "connection_name": null,
                        "dlq_event_queue_arn": null,
                        "event_queue_arn": null,
                        "exclusions": null,
                        "path": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw/",
                        "sample_size": null
                      }
                    ],
                    "schedule": null,
                    "schema_change_policy": [],
                    "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp",
                    "table_prefix": null,
                    "tags": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "Env": "sd"
                    },
                    "tags_all": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "Env": "sd"
                    }
                  },
                  "sensitive_values": {
                    "catalog_target": [],
                    "delta_target": [],
                    "dynamodb_target": [],
                    "hudi_target": [],
                    "iceberg_target": [],
                    "jdbc_target": [],
                    "lake_formation_configuration": [],
                    "lineage_configuration": [],
                    "mongodb_target": [],
                    "recrawl_policy": [],
                    "s3_target": [
                      {}
                    ],
                    "schema_change_policy": [],
                    "tags": {},
                    "tags_all": {}
                  }
                },
                {
                  "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_iam_role.role",
                  "mode": "managed",
                  "type": "aws_iam_role",
                  "name": "role",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
                    "description": null,
                    "force_detach_policies": false,
                    "max_session_duration": 3600,
                    "name": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-bp1.0.0",
                    "path": "/",
                    "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
                    "tags": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "Env": "sd"
                    },
                    "tags_all": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "Env": "sd"
                    }
                  },
                  "sensitive_values": {
                    "inline_policy": [],
                    "managed_policy_arns": [],
                    "tags": {},
                    "tags_all": {}
                  },
                  "identity_schema_version": 0,
                  "identity": {
                    "account_id": null,
                    "name": null
                  }
                },
                {
                  "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_iam_role_policy.glue_crawler_permissions",
                  "mode": "managed",
                  "type": "aws_iam_role_policy",
                  "name": "glue_crawler_permissions",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "name": "glue_crawler_permissions",
                    "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":\"s3:ListBucket\",\"Condition\":{\"StringLike\":{\"s3:prefix\":[\"raw//*\",\"raw/\"]}},\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0\",\"Sid\":\"S3ListBucket\"},{\"Action\":\"s3:GetObject\",\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw//*\",\"Sid\":\"S3ReadObjects\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:GetTables\",\"glue:GetTable\",\"glue:GetDatabases\",\"glue:GetDatabase\",\"glue:CreateTable\",\"glue:CreatePartition\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueCatalogDbTableAccess\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"],\"Sid\":\"GlueCrawlerLogs\"},{\"Action\":\"glue:GetSecurityConfiguration\",\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:security-configuration/eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp\",\"Sid\":\"GlueSecurityConfigurationAccess\"}]}"
                  },
                  "sensitive_values": {},
                  "identity_schema_version": 0,
                  "identity": {
                    "account_id": null,
                    "name": null,
                    "role": null
                  }
                }
              ],
              "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"]"
            },
            {
              "resources": [
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.aws_iam_policy.iam_policy[\"0\"]",
                  "mode": "managed",
                  "type": "aws_iam_policy",
                  "name": "iam_policy",
                  "index": "0",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "delay_after_policy_creation_in_ms": null,
                    "description": null,
                    "name": "policy_0_dpf-bp-artifacts",
                    "path": "/",
                    "tags": null
                  },
                  "sensitive_values": {
                    "tags_all": {}
                  },
                  "identity_schema_version": 0,
                  "identity": {
                    "arn": null
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket.s3_bucket",
                  "mode": "managed",
                  "type": "aws_s3_bucket",
                  "name": "s3_bucket",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts",
                    "force_destroy": true,
                    "region": "eu-west-1",
                    "tags": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "BuildingBlockName": "s3",
                      "BuildingBlockVersion": "1.1.0",
                      "Env": "sd",
                      "Name": "s3"
                    },
                    "tags_all": {
                      "ApplicationID": "2102",
                      "ApplicationName": "DATA PLATFORM FOUNDATION",
                      "BuildingBlockName": "s3",
                      "BuildingBlockVersion": "1.1.0",
                      "Env": "sd",
                      "Name": "s3"
                    },
                    "timeouts": null
                  },
                  "sensitive_values": {
                    "cors_rule": [],
                    "grant": [],
                    "lifecycle_rule": [],
                    "logging": [],
                    "object_lock_configuration": [],
                    "replication_configuration": [],
                    "server_side_encryption_configuration": [],
                    "tags": {},
                    "tags_all": {},
                    "versioning": [],
                    "website": []
                  },
                  "identity_schema_version": 0,
                  "identity": {
                    "account_id": null,
                    "bucket": null,
                    "region": null
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket_logging.example",
                  "mode": "managed",
                  "type": "aws_s3_bucket_logging",
                  "name": "example",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "expected_bucket_owner": null,
                    "region": "eu-west-1",
                    "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                    "target_grant": [],
                    "target_object_key_format": [
                      {
                        "partitioned_prefix": [
                          {
                            "partition_date_source": "EventTime"
                          }
                        ],
                        "simple_prefix": []
                      }
                    ],
                    "target_prefix": "log/"
                  },
                  "sensitive_values": {
                    "target_grant": [],
                    "target_object_key_format": [
                      {
                        "partitioned_prefix": [
                          {}
                        ],
                        "simple_prefix": []
                      }
                    ]
                  },
                  "identity_schema_version": 1,
                  "identity": {
                    "account_id": null,
                    "bucket": null,
                    "region": null
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket_policy.bucket_policy",
                  "mode": "managed",
                  "type": "aws_s3_bucket_policy",
                  "name": "bucket_policy",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "region": "eu-west-1"
                  },
                  "sensitive_values": {},
                  "identity_schema_version": 0,
                  "identity": {
                    "account_id": null,
                    "bucket": null,
                    "region": null
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket_public_access_block.public_access_block",
                  "mode": "managed",
                  "type": "aws_s3_bucket_public_access_block",
                  "name": "public_access_block",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "block_public_acls": true,
                    "block_public_policy": true,
                    "ignore_public_acls": true,
                    "region": "eu-west-1",
                    "restrict_public_buckets": true,
                    "skip_destroy": null
                  },
                  "sensitive_values": {},
                  "identity_schema_version": 0,
                  "identity": {
                    "account_id": null,
                    "bucket": null,
                    "region": null
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_prisma",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "allow_prisma",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": null,
                    "statement": [
                      {
                        "actions": [
                          "s3:GetAccelerateConfiguration",
                          "s3:GetAnalyticsConfiguration",
                          "s3:GetBucket*",
                          "s3:GetBucketAcl",
                          "s3:GetBucketCORS",
                          "s3:GetBucketLocation",
                          "s3:GetBucketLogging",
                          "s3:GetBucketObjectLockConfiguration",
                          "s3:GetBucketOwnershipControls",
                          "s3:GetBucketPolicy",
                          "s3:GetBucketPolicyStatus",
                          "s3:GetBucketPublicAccessBlock",
                          "s3:GetBucketTagging",
                          "s3:GetBucketVersioning",
                          "s3:GetBucketWebsite",
                          "s3:GetEncryptionConfiguration",
                          "s3:GetInventoryConfiguration",
                          "s3:GetLifecycleConfiguration",
                          "s3:GetMetricsConfiguration",
                          "s3:GetReplicationConfiguration",
                          "s3:ListBucket"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                            ],
                            "type": "AWS"
                          }
                        ],
                        "resources": [
                          null
                        ],
                        "sid": "AllowPrisma"
                      }
                    ],
                    "version": null
                  },
                  "sensitive_values": {
                    "statement": [
                      {
                        "actions": [
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false,
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false
                        ]
                      }
                    ]
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_prisma_object",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "allow_prisma_object",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": null,
                    "statement": [
                      {
                        "actions": [
                          "s3:GetObjectAcl",
                          "s3:GetObjectTagging",
                          "s3:GetObjectVersionAcl"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                            ],
                            "type": "AWS"
                          }
                        ],
                        "resources": [
                          null
                        ],
                        "sid": "AllowPrismaObject"
                      }
                    ],
                    "version": null
                  },
                  "sensitive_values": {
                    "statement": [
                      {
                        "actions": [
                          false,
                          false,
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false
                        ]
                      }
                    ]
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_public_through_f5",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "allow_public_through_f5",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": null,
                    "statement": [
                      {
                        "actions": [
                          "s3:GetObject"
                        ],
                        "condition": [
                          {
                            "test": "IpAddress",
                            "values": [
                              "10.68.98.160/27",
                              "10.68.98.128/27"
                            ],
                            "variable": "aws:VpcSourceIp"
                          },
                          {
                            "test": "StringEquals",
                            "values": [
                              "vpc-0fbd9e814ef60d4ac"
                            ],
                            "variable": "aws:SourceVpc"
                          }
                        ],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "*"
                            ],
                            "type": "*"
                          }
                        ],
                        "resources": [
                          null,
                          null
                        ],
                        "sid": "AllowPublicThroughF5"
                      }
                    ],
                    "version": null
                  },
                  "sensitive_values": {
                    "statement": [
                      {
                        "actions": [
                          false
                        ],
                        "condition": [
                          {
                            "values": [
                              false,
                              false
                            ]
                          },
                          {
                            "values": [
                              false
                            ]
                          }
                        ],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false,
                          false
                        ]
                      }
                    ]
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_ssl_only",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "allow_ssl_only",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": null,
                    "statement": [
                      {
                        "actions": [
                          "s3:*"
                        ],
                        "condition": [
                          {
                            "test": "Bool",
                            "values": [
                              "false"
                            ],
                            "variable": "aws:SecureTransport"
                          }
                        ],
                        "effect": "Deny",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "*"
                            ],
                            "type": "*"
                          }
                        ],
                        "resources": [
                          null,
                          null
                        ],
                        "sid": "AllowSSLOnly"
                      }
                    ],
                    "version": null
                  },
                  "sensitive_values": {
                    "statement": [
                      {
                        "actions": [
                          false
                        ],
                        "condition": [
                          {
                            "values": [
                              false
                            ]
                          }
                        ],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false,
                          false
                        ]
                      }
                    ]
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_vpc_source",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "allow_vpc_source",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": null,
                    "statement": [
                      {
                        "actions": [
                          "s3:*"
                        ],
                        "condition": [
                          {
                            "test": "StringEquals",
                            "values": [
                              "638883080465"
                            ],
                            "variable": "aws:VpceAccount"
                          }
                        ],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [
                          {
                            "identifiers": [
                              "*"
                            ],
                            "type": "*"
                          }
                        ],
                        "resources": [
                          null,
                          null
                        ],
                        "sid": "AllowActionsFromInsideVPC"
                      }
                    ],
                    "version": null
                  },
                  "sensitive_values": {
                    "statement": [
                      {
                        "actions": [
                          false
                        ],
                        "condition": [
                          {
                            "values": [
                              false
                            ]
                          }
                        ],
                        "not_principals": [],
                        "principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "resources": [
                          false,
                          false
                        ]
                      }
                    ]
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.combined",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "combined",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "statement": [],
                    "version": null
                  },
                  "sensitive_values": {
                    "source_policy_documents": [],
                    "statement": []
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.custom_iam_policy_document[\"0\"]",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "custom_iam_policy_document",
                  "index": "0",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": null,
                    "statement": [
                      {
                        "actions": [
                          "s3:*"
                        ],
                        "condition": [],
                        "effect": "Allow",
                        "not_actions": null,
                        "not_principals": [],
                        "not_resources": null,
                        "principals": [],
                        "resources": [
                          "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts",
                          "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts/*"
                        ],
                        "sid": "AllowAllS3Actions"
                      }
                    ],
                    "version": null
                  },
                  "sensitive_values": {
                    "statement": [
                      {
                        "actions": [
                          false
                        ],
                        "condition": [],
                        "not_principals": [],
                        "principals": [],
                        "resources": [
                          false,
                          false
                        ]
                      }
                    ]
                  }
                },
                {
                  "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.deny_not_principals",
                  "mode": "data",
                  "type": "aws_iam_policy_document",
                  "name": "deny_not_principals",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "override_json": null,
                    "override_policy_documents": null,
                    "policy_id": null,
                    "source_json": null,
                    "source_policy_documents": null,
                    "statement": [
                      {
                        "actions": [
                          "s3:*"
                        ],
                        "condition": [
                          {
                            "test": "BoolIfExists",
                            "values": [
                              "false"
                            ],
                            "variable": "aws:PrincipalIsAWSService"
                          },
                          {
                            "test": "NotIpAddress",
                            "values": [
                              "10.68.98.160/27",
                              "10.68.98.128/27"
                            ],
                            "variable": "aws:VpcSourceIp"
                          },
                          {
                            "test": "StringNotEquals",
                            "values": [
                              "638883080465"
                            ],
                            "variable": "aws:VpceAccount"
                          },
                          {
                            "test": "StringNotEquals",
                            "values": [
                              "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                            ],
                            "variable": "aws:PrincipalArn"
                          }
                        ],
                        "effect": "Deny",
                        "not_actions": null,
                        "not_principals": [
                          {
                            "identifiers": [
                              "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                            ],
                            "type": "AWS"
                          }
                        ],
                        "not_resources": null,
                        "principals": [],
                        "resources": [
                          null,
                          null
                        ],
                        "sid": "DenyNotPrincipals"
                      }
                    ],
                    "version": null
                  },
                  "sensitive_values": {
                    "statement": [
                      {
                        "actions": [
                          false
                        ],
                        "condition": [
                          {
                            "values": [
                              false
                            ]
                          },
                          {
                            "values": [
                              false,
                              false
                            ]
                          },
                          {
                            "values": [
                              false
                            ]
                          },
                          {
                            "values": [
                              false
                            ]
                          }
                        ],
                        "not_principals": [
                          {
                            "identifiers": [
                              false
                            ]
                          }
                        ],
                        "principals": [],
                        "resources": [
                          false,
                          false
                        ]
                      }
                    ]
                  }
                }
              ],
              "address": "module.blueprint.module.s3_bucket_artifacts"
            },
            {
              "resources": [
                {
                  "address": "module.blueprint.module.glue_catalog_database[\"raw_db\"].aws_glue_catalog_database.catalog",
                  "mode": "managed",
                  "type": "aws_glue_catalog_database",
                  "name": "catalog",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "description": "Glue database per i dati raw",
                    "federated_database": [],
                    "name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
                    "parameters": null,
                    "region": "eu-west-1",
                    "tags": {
                      "ApplicationID": "id",
                      "ApplicationName": "test",
                      "Env": "sd"
                    },
                    "tags_all": {
                      "ApplicationID": "id",
                      "ApplicationName": "test",
                      "Env": "sd"
                    },
                    "target_database": []
                  },
                  "sensitive_values": {
                    "create_table_default_permission": [],
                    "federated_database": [],
                    "tags": {},
                    "tags_all": {},
                    "target_database": []
                  }
                },
                {
                  "address": "module.blueprint.module.glue_catalog_database[\"raw_db\"].aws_iam_policy.iam_policy[\"0\"]",
                  "mode": "managed",
                  "type": "aws_iam_policy",
                  "name": "iam_policy",
                  "index": "0",
                  "provider_name": "registry.terraform.io/hashicorp/aws",
                  "schema_version": 0,
                  "values": {
                    "delay_after_policy_creation_in_ms": null,
                    "description": null,
                    "name": "policy_glue_db_0_raw",
                    "path": "/",
                    "policy": "{\"Statement\":[{\"Action\":[\"glue:GetTables\",\"glue:GetDatabase\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/raw_db/*\",\"arn:aws:glue:eu-west-1:899076912694:database/raw_db\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueDatabaseRead\"}],\"Version\":\"2012-10-17\"}",
                    "tags": null
                  },
                  "sensitive_values": {
                    "tags_all": {}
                  },
                  "identity_schema_version": 0,
                  "identity": {
                    "arn": null
                  }
                }
              ],
              "address": "module.blueprint.module.glue_catalog_database[\"raw_db\"]"
            }
          ]
        }
      ]
    }
  },
  "resource_changes": [
    {
      "address": "module.bb_blueprint.aws_cloudwatch_log_group.sf_logs",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_cloudwatch_log_group",
      "name": "sf_logs",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:logs:eu-west-1:899076912694:log-group:eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test",
          "deletion_protection_enabled": false,
          "id": "eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test",
          "kms_key_id": "arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
          "log_group_class": "STANDARD",
          "name": "eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test",
          "name_prefix": "",
          "region": "eu-west-1",
          "retention_in_days": 365,
          "skip_destroy": false,
          "tags": {},
          "tags_all": {}
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_cloudwatch_log_resource_policy.allow_sfn",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_cloudwatch_log_resource_policy",
      "name": "allow_sfn",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "id": "AllowStepFunctionsToWriteSFLogs",
          "policy_document": "{\"Statement\":[{\"Action\":[\"logs:CreateLogStream\",\"logs:PutLogEvents\",\"logs:DescribeLogStreams\"],\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"states.amazonaws.com\"},\"Resource\":\"arn:aws:logs:eu-west-1:899076912694:log-group:eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test:*\",\"Sid\":\"AllowSFN\"}],\"Version\":\"2012-10-17\"}",
          "policy_name": "AllowStepFunctionsToWriteSFLogs",
          "region": "eu-west-1"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_glue_catalog_table.databases[\"raw_db.logs.ExtractionErrors\"]",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_glue_catalog_table",
      "name": "databases",
      "index": "raw_db.logs.ExtractionErrors",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/extractionerrors",
          "catalog_id": "899076912694",
          "database_name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
          "description": "",
          "id": "899076912694:eniaws-glue-cat-euwe1-ictd-899076912694-raw:extractionerrors",
          "name": "extractionerrors",
          "open_table_format_input": [],
          "owner": "",
          "parameters": {
            "format-version": "2"
          },
          "partition_index": [],
          "partition_keys": [],
          "region": "eu-west-1",
          "retention": 0,
          "storage_descriptor": [
            {
              "additional_locations": [],
              "bucket_columns": [],
              "columns": [
                {
                  "comment": "",
                  "name": "entityname",
                  "parameters": {},
                  "type": "string"
                },
                {
                  "comment": "",
                  "name": "inputrowscount",
                  "parameters": {},
                  "type": "int"
                },
                {
                  "comment": "",
                  "name": "errorrowscount",
                  "parameters": {},
                  "type": "int"
                },
                {
                  "comment": "",
                  "name": "slicedate",
                  "parameters": {},
                  "type": "timestamp"
                },
                {
                  "comment": "",
                  "name": "runid",
                  "parameters": {},
                  "type": "string"
                },
                {
                  "comment": "",
                  "name": "isfullloading",
                  "parameters": {},
                  "type": "string"
                }
              ],
              "compressed": false,
              "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
              "location": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/logs/ExtractionErrors/",
              "number_of_buckets": 0,
              "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
              "parameters": {},
              "schema_reference": [],
              "ser_de_info": [
                {
                  "name": "",
                  "parameters": {
                    "serialization.format": "1"
                  },
                  "serialization_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe"
                }
              ],
              "skewed_info": [],
              "sort_columns": [],
              "stored_as_sub_directories": false
            }
          ],
          "table_type": "ICEBERG",
          "target_table": [],
          "view_expanded_text": "",
          "view_original_text": ""
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "open_table_format_input": [],
          "parameters": {},
          "partition_index": [],
          "partition_keys": [],
          "storage_descriptor": [
            {
              "additional_locations": [],
              "bucket_columns": [],
              "columns": [
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                }
              ],
              "parameters": {},
              "schema_reference": [],
              "ser_de_info": [
                {
                  "parameters": {}
                }
              ],
              "skewed_info": [],
              "sort_columns": []
            }
          ],
          "target_table": []
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_glue_catalog_table.databases[\"raw_db.logs.ExtractionErrorsDetail\"]",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_glue_catalog_table",
      "name": "databases",
      "index": "raw_db.logs.ExtractionErrorsDetail",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/extractionerrorsdetail",
          "catalog_id": "899076912694",
          "database_name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
          "description": "",
          "id": "899076912694:eniaws-glue-cat-euwe1-ictd-899076912694-raw:extractionerrorsdetail",
          "name": "extractionerrorsdetail",
          "open_table_format_input": [],
          "owner": "",
          "parameters": {
            "format-version": "2"
          },
          "partition_index": [],
          "partition_keys": [],
          "region": "eu-west-1",
          "retention": 0,
          "storage_descriptor": [
            {
              "additional_locations": [],
              "bucket_columns": [],
              "columns": [
                {
                  "comment": "",
                  "name": "entityname",
                  "parameters": {},
                  "type": "string"
                },
                {
                  "comment": "",
                  "name": "pk",
                  "parameters": {},
                  "type": "string"
                },
                {
                  "comment": "",
                  "name": "exceptions",
                  "parameters": {},
                  "type": "string"
                },
                {
                  "comment": "",
                  "name": "loadingslicedate",
                  "parameters": {},
                  "type": "string"
                },
                {
                  "comment": "",
                  "name": "auditinputfile",
                  "parameters": {},
                  "type": "string"
                },
                {
                  "comment": "",
                  "name": "auditfilecreationdatetime",
                  "parameters": {},
                  "type": "timestamp"
                },
                {
                  "comment": "",
                  "name": "auditcurrentdatetime",
                  "parameters": {},
                  "type": "timestamp"
                },
                {
                  "comment": "",
                  "name": "auditslicedate",
                  "parameters": {},
                  "type": "string"
                },
                {
                  "comment": "",
                  "name": "auditrunid",
                  "parameters": {},
                  "type": "string"
                },
                {
                  "comment": "",
                  "name": "auditisfullloading",
                  "parameters": {},
                  "type": "string"
                }
              ],
              "compressed": false,
              "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
              "location": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/logs/ExtractionErrorsDetail/",
              "number_of_buckets": 0,
              "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
              "parameters": {},
              "schema_reference": [],
              "ser_de_info": [
                {
                  "name": "",
                  "parameters": {
                    "serialization.format": "1"
                  },
                  "serialization_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe"
                }
              ],
              "skewed_info": [],
              "sort_columns": [],
              "stored_as_sub_directories": false
            }
          ],
          "table_type": "ICEBERG",
          "target_table": [],
          "view_expanded_text": "",
          "view_original_text": ""
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "open_table_format_input": [],
          "parameters": {},
          "partition_index": [],
          "partition_keys": [],
          "storage_descriptor": [
            {
              "additional_locations": [],
              "bucket_columns": [],
              "columns": [
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                },
                {
                  "parameters": {}
                }
              ],
              "parameters": {},
              "schema_reference": [],
              "ser_de_info": [
                {
                  "parameters": {}
                }
              ],
              "skewed_info": [],
              "sort_columns": []
            }
          ],
          "target_table": []
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_iam_role.step_function_role[0]",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_iam_role",
      "name": "step_function_role",
      "index": 0,
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:role/eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp",
          "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"states.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
          "create_date": "2026-02-13T15:23:45Z",
          "description": "",
          "force_detach_policies": false,
          "id": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp",
          "inline_policy": [
            {
              "name": "eniaws-sfn-role-euwe1-ictd-899076912694-dpf-bp",
              "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"sns:Publish\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp\"}]}"
            },
            {
              "name": "step-function-policy",
              "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"lambda:InvokeFunction\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"},{\"Action\":[\"logs:CreateLogDelivery\",\"logs:GetLogDelivery\",\"logs:UpdateLogDelivery\",\"logs:DeleteLogDelivery\",\"logs:ListLogDeliveries\",\"logs:PutResourcePolicy\",\"logs:DescribeResourcePolicies\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:PutLogEvents\",\"logs:DescribeLogStreams\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test:*\"]},{\"Action\":[\"kms:Decrypt\",\"kms:Encrypt\",\"kms:GenerateDataKey\",\"kms:DescribeKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343\"]}]}"
            }
          ],
          "managed_policy_arns": [],
          "max_session_duration": 3600,
          "name": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp",
          "name_prefix": "",
          "path": "/",
          "permissions_boundary": "",
          "tags": {},
          "tags_all": {},
          "unique_id": "AROA5CVJI6Y3GYQS2BVSA"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "inline_policy": [
            {},
            {}
          ],
          "managed_policy_arns": [],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_iam_role_policy.sfn_publish_sns[0]",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_iam_role_policy",
      "name": "sfn_publish_sns",
      "index": 0,
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "id": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp:eniaws-sfn-role-euwe1-ictd-899076912694-dpf-bp",
          "name": "eniaws-sfn-role-euwe1-ictd-899076912694-dpf-bp",
          "name_prefix": "",
          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"sns:Publish\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp\"}]}",
          "role": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "eniaws-sfn-role-euwe1-ictd-899076912694-dpf-bp",
          "role": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_iam_role_policy.step_function_policy[0]",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_iam_role_policy",
      "name": "step_function_policy",
      "index": 0,
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "id": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp:step-function-policy",
          "name": "step-function-policy",
          "name_prefix": "",
          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"lambda:InvokeFunction\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"},{\"Action\":[\"logs:CreateLogDelivery\",\"logs:GetLogDelivery\",\"logs:UpdateLogDelivery\",\"logs:DeleteLogDelivery\",\"logs:ListLogDeliveries\",\"logs:PutResourcePolicy\",\"logs:DescribeResourcePolicies\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:PutLogEvents\",\"logs:DescribeLogStreams\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test:*\"]},{\"Action\":[\"kms:Decrypt\",\"kms:Encrypt\",\"kms:GenerateDataKey\",\"kms:DescribeKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343\"]}]}",
          "role": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "step-function-policy",
          "role": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_kms_alias.logs",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_kms_alias",
      "name": "logs",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:kms:eu-west-1:899076912694:alias/dp1453",
          "id": "alias/dp1453",
          "name": "alias/dp1453",
          "name_prefix": "",
          "region": "eu-west-1",
          "target_key_arn": "arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
          "target_key_id": "3c1b5c53-3d2d-4fd9-9889-93ba148e6343"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "alias/dp1453",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_kms_key.logs",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_kms_key",
      "name": "logs",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
          "bypass_policy_lockout_safety_check": false,
          "custom_key_store_id": "",
          "customer_master_key_spec": "SYMMETRIC_DEFAULT",
          "deletion_window_in_days": 7,
          "description": "CMK for CloudWatch Logs encryption",
          "enable_key_rotation": true,
          "id": "3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
          "is_enabled": true,
          "key_id": "3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
          "key_usage": "ENCRYPT_DECRYPT",
          "multi_region": false,
          "policy": "{\"Statement\":[{\"Action\":\"kms:*\",\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:root\"},\"Resource\":\"*\",\"Sid\":\"EnableRootPermissions\"},{\"Action\":[\"kms:Encrypt\",\"kms:Decrypt\",\"kms:ReEncrypt*\",\"kms:GenerateDataKey*\",\"kms:DescribeKey\"],\"Condition\":{\"ArnLike\":{\"kms:EncryptionContext:aws:logs:arn\":\"arn:aws:logs:eu-west-1:899076912694:log-group:*\"}},\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"logs.eu-west-1.amazonaws.com\"},\"Resource\":\"*\",\"Sid\":\"AllowCloudWatchLogsUseOfKey\"},{\"Action\":[\"kms:Encrypt\",\"kms:Decrypt\",\"kms:ReEncrypt*\",\"kms:GenerateDataKey*\",\"kms:DescribeKey\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp\"},\"Resource\":\"*\",\"Sid\":\"AllowStepFunctionUseOfKey\"},{\"Action\":[\"kms:CreateGrant\",\"kms:ListGrants\",\"kms:RevokeGrant\"],\"Condition\":{\"Bool\":{\"kms:GrantIsForAWSResource\":\"true\"}},\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"logs.eu-west-1.amazonaws.com\"},\"Resource\":\"*\",\"Sid\":\"AllowCloudWatchLogsGrants\"},{\"Action\":[\"kms:Encrypt\",\"kms:Decrypt\",\"kms:ReEncrypt*\",\"kms:GenerateDataKey*\",\"kms:DescribeKey\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp\"},\"Resource\":\"*\",\"Sid\":\"AllowStepFunctionUseOfKey\"}],\"Version\":\"2012-10-17\"}",
          "region": "eu-west-1",
          "rotation_period_in_days": 365,
          "tags": {},
          "tags_all": {},
          "timeouts": null,
          "xks_key_id": ""
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "id": "3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_s3_bucket_notification.notify_lambda",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_s3_bucket_notification",
      "name": "notify_lambda",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "eventbridge": false,
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "lambda_function": [
            {
              "events": [
                "s3:ObjectCreated:*"
              ],
              "filter_prefix": "",
              "filter_suffix": "",
              "id": "tf-s3-lambda-20260212093842339000000001",
              "lambda_function_arn": "arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test"
            }
          ],
          "queue": [],
          "region": "eu-west-1",
          "topic": []
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "lambda_function": [
            {
              "events": [
                false
              ]
            }
          ],
          "queue": [],
          "topic": []
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.aws_sns_topic.error_notification",
      "module_address": "module.bb_blueprint",
      "mode": "managed",
      "type": "aws_sns_topic",
      "name": "error_notification",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "application_failure_feedback_role_arn": "",
          "application_success_feedback_role_arn": "",
          "application_success_feedback_sample_rate": 0,
          "archive_policy": "",
          "arn": "arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp",
          "beginning_archive_time": "",
          "content_based_deduplication": false,
          "delivery_policy": "",
          "display_name": "",
          "fifo_throughput_scope": "",
          "fifo_topic": false,
          "firehose_failure_feedback_role_arn": "",
          "firehose_success_feedback_role_arn": "",
          "firehose_success_feedback_sample_rate": 0,
          "http_failure_feedback_role_arn": "",
          "http_success_feedback_role_arn": "",
          "http_success_feedback_sample_rate": 0,
          "id": "arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp",
          "kms_master_key_id": "alias/aws/sns",
          "lambda_failure_feedback_role_arn": "",
          "lambda_success_feedback_role_arn": "",
          "lambda_success_feedback_sample_rate": 0,
          "name": "eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp",
          "name_prefix": "",
          "owner": "899076912694",
          "policy": "{\"Id\":\"__default_policy_ID\",\"Statement\":[{\"Action\":[\"SNS:GetTopicAttributes\",\"SNS:SetTopicAttributes\",\"SNS:AddPermission\",\"SNS:RemovePermission\",\"SNS:DeleteTopic\",\"SNS:Subscribe\",\"SNS:ListSubscriptionsByTopic\",\"SNS:Publish\"],\"Condition\":{\"StringEquals\":{\"AWS:SourceOwner\":\"899076912694\"}},\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"*\"},\"Resource\":\"arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp\",\"Sid\":\"__default_statement_ID\"}],\"Version\":\"2008-10-17\"}",
          "region": "eu-west-1",
          "signature_version": 0,
          "sqs_failure_feedback_role_arn": "",
          "sqs_success_feedback_role_arn": "",
          "sqs_success_feedback_sample_rate": 0,
          "tags": {},
          "tags_all": {},
          "tracing_config": ""
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "arn": "arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.blueprint.aws_glue_catalog_table.databases[\"raw_db.logs.ExtractionErrors\"]",
      "module_address": "module.blueprint",
      "mode": "managed",
      "type": "aws_glue_catalog_table",
      "name": "databases",
      "index": "raw_db.logs.ExtractionErrors",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "database_name": "raw_db",
          "description": null,
          "name": "extractionerrors",
          "open_table_format_input": [],
          "owner": null,
          "parameters": {
            "format-version": "2",
            "table_type": "ICEBERG"
          },
          "partition_keys": [],
          "region": "eu-west-1",
          "retention": null,
          "storage_descriptor": [
            {
              "additional_locations": null,
              "bucket_columns": null,
              "columns": [
                {
                  "comment": null,
                  "name": "EntityName",
                  "parameters": null,
                  "type": "string"
                },
                {
                  "comment": null,
                  "name": "InputRowsCount",
                  "parameters": null,
                  "type": "int"
                },
                {
                  "comment": null,
                  "name": "ErrorRowsCount",
                  "parameters": null,
                  "type": "int"
                },
                {
                  "comment": null,
                  "name": "SliceDate",
                  "parameters": null,
                  "type": "timestamp"
                },
                {
                  "comment": null,
                  "name": "RunId",
                  "parameters": null,
                  "type": "string"
                },
                {
                  "comment": null,
                  "name": "IsFullLoading",
                  "parameters": null,
                  "type": "string"
                }
              ],
              "compressed": null,
              "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
              "location": "s3://eniaws-s3-euwe1-ictd-899076912694-s3-access-logs/logs/ExtractionErrors/",
              "number_of_buckets": null,
              "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
              "parameters": null,
              "schema_reference": [],
              "ser_de_info": [
                {
                  "name": null,
                  "parameters": {
                    "serialization.format": "1"
                  },
                  "serialization_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe"
                }
              ],
              "skewed_info": [],
              "sort_columns": [],
              "stored_as_sub_directories": null
            }
          ],
          "table_type": "ICEBERG",
          "target_table": [],
          "view_expanded_text": null,
          "view_original_text": null
        },
        "after_unknown": {
          "arn": true,
          "catalog_id": true,
          "id": true,
          "open_table_format_input": [],
          "parameters": {},
          "partition_index": true,
          "partition_keys": [],
          "storage_descriptor": [
            {
              "columns": [
                {},
                {},
                {},
                {},
                {},
                {}
              ],
              "schema_reference": [],
              "ser_de_info": [
                {
                  "parameters": {}
                }
              ],
              "skewed_info": [],
              "sort_columns": []
            }
          ],
          "target_table": []
        },
        "before_sensitive": false,
        "after_sensitive": {
          "open_table_format_input": [],
          "parameters": {},
          "partition_index": [],
          "partition_keys": [],
          "storage_descriptor": [
            {
              "columns": [
                {},
                {},
                {},
                {},
                {},
                {}
              ],
              "schema_reference": [],
              "ser_de_info": [
                {
                  "parameters": {}
                }
              ],
              "skewed_info": [],
              "sort_columns": []
            }
          ],
          "target_table": []
        }
      }
    },
    {
      "address": "module.blueprint.aws_glue_catalog_table.databases[\"raw_db.logs.ExtractionErrorsDetail\"]",
      "module_address": "module.blueprint",
      "mode": "managed",
      "type": "aws_glue_catalog_table",
      "name": "databases",
      "index": "raw_db.logs.ExtractionErrorsDetail",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "database_name": "raw_db",
          "description": null,
          "name": "extractionerrorsdetail",
          "open_table_format_input": [],
          "owner": null,
          "parameters": {
            "format-version": "2",
            "table_type": "ICEBERG"
          },
          "partition_keys": [],
          "region": "eu-west-1",
          "retention": null,
          "storage_descriptor": [
            {
              "additional_locations": null,
              "bucket_columns": null,
              "columns": [
                {
                  "comment": null,
                  "name": "EntityName",
                  "parameters": null,
                  "type": "string"
                },
                {
                  "comment": null,
                  "name": "PK",
                  "parameters": null,
                  "type": "string"
                },
                {
                  "comment": null,
                  "name": "Exceptions",
                  "parameters": null,
                  "type": "string"
                },
                {
                  "comment": null,
                  "name": "LoadingSliceDate",
                  "parameters": null,
                  "type": "string"
                },
                {
                  "comment": null,
                  "name": "AuditInputFile",
                  "parameters": null,
                  "type": "string"
                },
                {
                  "comment": null,
                  "name": "AuditFileCreationDatetime",
                  "parameters": null,
                  "type": "timestamp"
                },
                {
                  "comment": null,
                  "name": "AuditCurrentDatetime",
                  "parameters": null,
                  "type": "timestamp"
                },
                {
                  "comment": null,
                  "name": "AuditSliceDate",
                  "parameters": null,
                  "type": "string"
                },
                {
                  "comment": null,
                  "name": "AuditRunId",
                  "parameters": null,
                  "type": "string"
                },
                {
                  "comment": null,
                  "name": "AuditIsFullLoading",
                  "parameters": null,
                  "type": "string"
                }
              ],
              "compressed": null,
              "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
              "location": "s3://eniaws-s3-euwe1-ictd-899076912694-s3-access-logs/logs/ExtractionErrorsDetail/",
              "number_of_buckets": null,
              "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
              "parameters": null,
              "schema_reference": [],
              "ser_de_info": [
                {
                  "name": null,
                  "parameters": {
                    "serialization.format": "1"
                  },
                  "serialization_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe"
                }
              ],
              "skewed_info": [],
              "sort_columns": [],
              "stored_as_sub_directories": null
            }
          ],
          "table_type": "ICEBERG",
          "target_table": [],
          "view_expanded_text": null,
          "view_original_text": null
        },
        "after_unknown": {
          "arn": true,
          "catalog_id": true,
          "id": true,
          "open_table_format_input": [],
          "parameters": {},
          "partition_index": true,
          "partition_keys": [],
          "storage_descriptor": [
            {
              "columns": [
                {},
                {},
                {},
                {},
                {},
                {},
                {},
                {},
                {},
                {}
              ],
              "schema_reference": [],
              "ser_de_info": [
                {
                  "parameters": {}
                }
              ],
              "skewed_info": [],
              "sort_columns": []
            }
          ],
          "target_table": []
        },
        "before_sensitive": false,
        "after_sensitive": {
          "open_table_format_input": [],
          "parameters": {},
          "partition_index": [],
          "partition_keys": [],
          "storage_descriptor": [
            {
              "columns": [
                {},
                {},
                {},
                {},
                {},
                {},
                {},
                {},
                {},
                {}
              ],
              "schema_reference": [],
              "ser_de_info": [
                {
                  "parameters": {}
                }
              ],
              "skewed_info": [],
              "sort_columns": []
            }
          ],
          "target_table": []
        }
      }
    },
    {
      "address": "module.bb_blueprint.module.glue_catalog_database[\"raw_db\"].aws_glue_catalog_database.catalog",
      "module_address": "module.bb_blueprint.module.glue_catalog_database[\"raw_db\"]",
      "mode": "managed",
      "type": "aws_glue_catalog_database",
      "name": "catalog",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw",
          "catalog_id": "899076912694",
          "create_table_default_permission": [
            {
              "permissions": [
                "ALL"
              ],
              "principal": [
                {
                  "data_lake_principal_identifier": "IAM_ALLOWED_PRINCIPALS"
                }
              ]
            }
          ],
          "description": "Glue database per i dati raw",
          "federated_database": [],
          "id": "899076912694:eniaws-glue-cat-euwe1-ictd-899076912694-raw",
          "location_uri": "",
          "name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
          "parameters": {},
          "region": "eu-west-1",
          "tags": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "Env": "sd"
          },
          "tags_all": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "Env": "sd"
          },
          "target_database": []
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "create_table_default_permission": [
            {
              "permissions": [
                false
              ],
              "principal": [
                {}
              ]
            }
          ],
          "federated_database": [],
          "parameters": {},
          "tags": {},
          "tags_all": {},
          "target_database": []
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_catalog_database[\"raw_db\"].aws_iam_policy.iam_policy[\"0\"]",
      "module_address": "module.bb_blueprint.module.glue_catalog_database[\"raw_db\"]",
      "mode": "managed",
      "type": "aws_iam_policy",
      "name": "iam_policy",
      "index": "0",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:policy/policy_glue_db_0_raw",
          "attachment_count": 0,
          "delay_after_policy_creation_in_ms": null,
          "description": "",
          "id": "arn:aws:iam::899076912694:policy/policy_glue_db_0_raw",
          "name": "policy_glue_db_0_raw",
          "name_prefix": "",
          "path": "/",
          "policy": "{\"Statement\":[{\"Action\":[\"glue:GetTables\",\"glue:GetDatabase\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/raw_db/*\",\"arn:aws:glue:eu-west-1:899076912694:database/raw_db\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueDatabaseRead\"}],\"Version\":\"2012-10-17\"}",
          "policy_id": "ANPA5CVJI6Y3OPADRRZ46",
          "tags": {},
          "tags_all": {}
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "arn": "arn:aws:iam::899076912694:policy/policy_glue_db_0_raw"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"].aws_glue_crawler.crawler",
      "module_address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"]",
      "mode": "managed",
      "type": "aws_glue_crawler",
      "name": "crawler",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:glue:eu-west-1:899076912694:crawler/eniaws-glue-crw-euwe1-ictd-899076912694-dpf-bp",
          "catalog_target": [],
          "classifiers": [],
          "configuration": "",
          "database_name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
          "delta_target": [],
          "description": "",
          "dynamodb_target": [],
          "hudi_target": [],
          "iceberg_target": [],
          "id": "eniaws-glue-crw-euwe1-ictd-899076912694-dpf-bp",
          "jdbc_target": [],
          "lake_formation_configuration": [
            {
              "account_id": "",
              "use_lake_formation_credentials": false
            }
          ],
          "lineage_configuration": [
            {
              "crawler_lineage_settings": "ENABLE"
            }
          ],
          "mongodb_target": [],
          "name": "eniaws-glue-crw-euwe1-ictd-899076912694-dpf-bp",
          "recrawl_policy": [
            {
              "recrawl_behavior": "CRAWL_EVERYTHING"
            }
          ],
          "region": "eu-west-1",
          "role": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp",
          "s3_target": [
            {
              "connection_name": "",
              "dlq_event_queue_arn": "",
              "event_queue_arn": "",
              "exclusions": [],
              "path": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/raw/",
              "sample_size": 0
            }
          ],
          "schedule": "cron(0 12 * * ? *)",
          "schema_change_policy": [
            {
              "delete_behavior": "LOG",
              "update_behavior": "UPDATE_IN_DATABASE"
            }
          ],
          "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l1-l2",
          "table_prefix": "sd_",
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd",
            "Name": "glue_crawler"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd",
            "Name": "glue_crawler"
          }
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "catalog_target": [],
          "classifiers": [],
          "delta_target": [],
          "dynamodb_target": [],
          "hudi_target": [],
          "iceberg_target": [],
          "jdbc_target": [],
          "lake_formation_configuration": [
            {}
          ],
          "lineage_configuration": [
            {}
          ],
          "mongodb_target": [],
          "recrawl_policy": [
            {}
          ],
          "s3_target": [
            {
              "exclusions": []
            }
          ],
          "schema_change_policy": [
            {}
          ],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"].aws_iam_role.role",
      "module_address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"]",
      "mode": "managed",
      "type": "aws_iam_role",
      "name": "role",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:role/eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp",
          "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
          "create_date": "2026-02-12T09:35:21Z",
          "description": "",
          "force_detach_policies": false,
          "id": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp",
          "inline_policy": [
            {
              "name": "glue_crawler_permissions",
              "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":\"s3:ListBucket\",\"Condition\":{\"StringLike\":{\"s3:prefix\":[\"raw//*\",\"raw/\"]}},\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"Sid\":\"S3ListBucket\"},{\"Action\":\"s3:GetObject\",\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/raw//*\",\"Sid\":\"S3ReadObjects\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:GetTables\",\"glue:GetTable\",\"glue:GetDatabases\",\"glue:GetDatabase\",\"glue:CreateTable\",\"glue:CreatePartition\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueCatalogDbTableAccess\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"],\"Sid\":\"GlueCrawlerLogs\"},{\"Action\":[\"glue:GetSecurityConfigurations\",\"glue:GetSecurityConfiguration\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"GlueSecurityConfigurationAccess\"},{\"Action\":\"glue:GetSecurityConfiguration\",\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"AllowGetSecurityConfiguration\"}]}"
            }
          ],
          "managed_policy_arns": [],
          "max_session_duration": 3600,
          "name": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp",
          "name_prefix": "",
          "path": "/",
          "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd",
            "Name": "glue_crawler"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd",
            "Name": "glue_crawler"
          },
          "unique_id": "AROA5CVJI6Y3NYCDVCJQX"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "inline_policy": [
            {}
          ],
          "managed_policy_arns": [],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"].aws_iam_role_policy.glue_crawler_permissions",
      "module_address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"]",
      "mode": "managed",
      "type": "aws_iam_role_policy",
      "name": "glue_crawler_permissions",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "id": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp:glue_crawler_permissions",
          "name": "glue_crawler_permissions",
          "name_prefix": "",
          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":\"s3:ListBucket\",\"Condition\":{\"StringLike\":{\"s3:prefix\":[\"raw//*\",\"raw/\"]}},\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"Sid\":\"S3ListBucket\"},{\"Action\":\"s3:GetObject\",\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/raw//*\",\"Sid\":\"S3ReadObjects\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:GetTables\",\"glue:GetTable\",\"glue:GetDatabases\",\"glue:GetDatabase\",\"glue:CreateTable\",\"glue:CreatePartition\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueCatalogDbTableAccess\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"],\"Sid\":\"GlueCrawlerLogs\"},{\"Action\":[\"glue:GetSecurityConfigurations\",\"glue:GetSecurityConfiguration\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"GlueSecurityConfigurationAccess\"},{\"Action\":\"glue:GetSecurityConfiguration\",\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"AllowGetSecurityConfiguration\"}]}",
          "role": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "glue_crawler_permissions",
          "role": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_1.aws_glue_connection.network",
      "module_address": "module.bb_blueprint.module.glue_job_1",
      "mode": "managed",
      "type": "aws_glue_connection",
      "name": "network",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
          "athena_properties": {},
          "catalog_id": "899076912694",
          "connection_properties": {},
          "connection_type": "NETWORK",
          "description": "",
          "id": "899076912694:eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
          "match_criteria": [],
          "name": "eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
          "physical_connection_requirements": [
            {
              "availability_zone": "eu-west-1a",
              "security_group_id_list": [
                "sg-032c47f80254c35c7",
                "sg-09096e91dd18fa7d4",
                "sg-0aa6fd5972038141a",
                "sg-0cb505f744b1c74eb"
              ],
              "subnet_id": "subnet-0a8409260cbaf999f"
            }
          ],
          "region": "eu-west-1",
          "tags": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "env",
            "Name": "job1"
          },
          "tags_all": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "env",
            "Name": "job1"
          }
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "athena_properties": true,
          "connection_properties": true,
          "match_criteria": [],
          "physical_connection_requirements": [
            {
              "security_group_id_list": [
                false,
                false,
                false,
                false
              ]
            }
          ],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_1.aws_glue_job.job",
      "module_address": "module.bb_blueprint.module.glue_job_1",
      "mode": "managed",
      "type": "aws_glue_job",
      "name": "job",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:glue:eu-west-1:899076912694:job/eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
          "command": [
            {
              "name": "glueetl",
              "python_version": "3",
              "runtime": "",
              "script_location": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/glue_jobs/src/extraction.py"
            }
          ],
          "connections": [
            "eniaws-glue-euwe1-ictd-899076912694-job-l0-l1"
          ],
          "default_arguments": {
            "--continuous-log-logGroup": "/aws-glue/jobs",
            "--enable-auto-scaling": "true",
            "--enable-continuous-cloudwatch-log": "true",
            "--enable-continuous-log-filter": "true",
            "--enable-job-insights": "true",
            "--enable-metrics": "",
            "--enable-observability-metrics": "true",
            "--input_path": "",
            "--job-language": "python",
            "--output_path": ""
          },
          "description": "Glue Job",
          "execution_class": "STANDARD",
          "execution_property": [
            {
              "max_concurrent_runs": 1
            }
          ],
          "glue_version": "4.0",
          "id": "eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
          "job_mode": "SCRIPT",
          "job_run_queuing_enabled": false,
          "maintenance_window": "",
          "max_capacity": 10,
          "max_retries": 0,
          "name": "eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
          "non_overridable_arguments": {},
          "notification_property": [],
          "number_of_workers": 10,
          "region": "eu-west-1",
          "role_arn": "arn:aws:iam::899076912694:role/eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1",
          "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l0-l1",
          "source_control_details": [],
          "tags": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "env",
            "Name": "job1"
          },
          "tags_all": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "env",
            "Name": "job1"
          },
          "timeout": 2880,
          "worker_type": "G.1X"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "command": [
            {}
          ],
          "connections": [
            false
          ],
          "default_arguments": {},
          "execution_property": [
            {}
          ],
          "non_overridable_arguments": {},
          "notification_property": [],
          "source_control_details": [],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_1.aws_glue_security_configuration.this",
      "module_address": "module.bb_blueprint.module.glue_job_1",
      "mode": "managed",
      "type": "aws_glue_security_configuration",
      "name": "this",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "encryption_configuration": [
            {
              "cloudwatch_encryption": [
                {
                  "cloudwatch_encryption_mode": "SSE-KMS",
                  "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/logs"
                }
              ],
              "job_bookmarks_encryption": [
                {
                  "job_bookmarks_encryption_mode": "CSE-KMS",
                  "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/glue"
                }
              ],
              "s3_encryption": [
                {
                  "kms_key_arn": "",
                  "s3_encryption_mode": "SSE-S3"
                }
              ]
            }
          ],
          "id": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l0-l1",
          "name": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l0-l1",
          "region": "eu-west-1"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "encryption_configuration": [
            {
              "cloudwatch_encryption": [
                {}
              ],
              "job_bookmarks_encryption": [
                {}
              ],
              "s3_encryption": [
                {}
              ]
            }
          ]
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_1.aws_iam_role.role",
      "module_address": "module.bb_blueprint.module.glue_job_1",
      "mode": "managed",
      "type": "aws_iam_role",
      "name": "role",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:role/eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1",
          "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
          "create_date": "2026-02-12T09:35:20Z",
          "description": "",
          "force_detach_policies": false,
          "id": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1",
          "inline_policy": [
            {
              "name": "glue_job_permissions",
              "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"s3:PutObject\",\"s3:ListBucket\",\"s3:GetObject\",\"s3:GetBucketLocation\",\"s3:DeleteObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"S3Access\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"LogsAccess\"},{\"Action\":\"cloudwatch:PutMetricData\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"CloudWatchMetrics\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:SearchTables\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"GlueAccess\"},{\"Action\":[\"ec2:GetConnectionStatus\",\"ec2:Describe*\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"EC2Describe\"},{\"Action\":[\"ec2:DetachNetworkInterface\",\"ec2:DeleteNetworkInterface\",\"ec2:CreateNetworkInterface\",\"ec2:AttachNetworkInterface\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7\",\"arn:aws:ec2:eu-west-1:899076912694:network-interface/*\"],\"Sid\":\"EC2Modify\"},{\"Action\":[\"glue:GetConnections\",\"glue:GetConnection\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l0-l1\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueConnectionRead\"},{\"Action\":[\"ec2:DescribeVpcs\",\"ec2:DescribeVpcEndpoints\",\"ec2:DescribeSubnets\",\"ec2:DescribeSecurityGroups\",\"ec2:DescribeRouteTables\",\"ec2:DescribeNetworkInterfaces\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"EC2DescribeForGlueNetwork\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"AllowRestrictedGlueActions\"},{\"Action\":[\"logs:DisassociateKmsKey\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*\",\"arn:aws:kms:eu-west-1:899076912694:alias/aws/glue\"],\"Sid\":\"AllowCloudWatchLogsAssociateKmsKey\"}]}"
            }
          ],
          "managed_policy_arns": [],
          "max_session_duration": 3600,
          "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1",
          "name_prefix": "",
          "path": "/",
          "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
          "tags": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "Env": "env",
            "Name": "job1"
          },
          "tags_all": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "Env": "env",
            "Name": "job1"
          },
          "unique_id": "AROA5CVJI6Y3ANO43V6JZ"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "inline_policy": [
            {}
          ],
          "managed_policy_arns": [],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_1.aws_iam_role_policy.glue_job_permissions",
      "module_address": "module.bb_blueprint.module.glue_job_1",
      "mode": "managed",
      "type": "aws_iam_role_policy",
      "name": "glue_job_permissions",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "id": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1:glue_job_permissions",
          "name": "glue_job_permissions",
          "name_prefix": "",
          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"s3:PutObject\",\"s3:ListBucket\",\"s3:GetObject\",\"s3:GetBucketLocation\",\"s3:DeleteObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"S3Access\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"LogsAccess\"},{\"Action\":\"cloudwatch:PutMetricData\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"CloudWatchMetrics\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:SearchTables\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"GlueAccess\"},{\"Action\":[\"ec2:GetConnectionStatus\",\"ec2:Describe*\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"EC2Describe\"},{\"Action\":[\"ec2:DetachNetworkInterface\",\"ec2:DeleteNetworkInterface\",\"ec2:CreateNetworkInterface\",\"ec2:AttachNetworkInterface\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7\",\"arn:aws:ec2:eu-west-1:899076912694:network-interface/*\"],\"Sid\":\"EC2Modify\"},{\"Action\":[\"glue:GetConnections\",\"glue:GetConnection\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l0-l1\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueConnectionRead\"},{\"Action\":[\"ec2:DescribeVpcs\",\"ec2:DescribeVpcEndpoints\",\"ec2:DescribeSubnets\",\"ec2:DescribeSecurityGroups\",\"ec2:DescribeRouteTables\",\"ec2:DescribeNetworkInterfaces\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"EC2DescribeForGlueNetwork\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"AllowRestrictedGlueActions\"},{\"Action\":[\"logs:DisassociateKmsKey\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*\",\"arn:aws:kms:eu-west-1:899076912694:alias/aws/glue\"],\"Sid\":\"AllowCloudWatchLogsAssociateKmsKey\"}]}",
          "role": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "glue_job_permissions",
          "role": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_2.aws_glue_connection.network",
      "module_address": "module.bb_blueprint.module.glue_job_2",
      "mode": "managed",
      "type": "aws_glue_connection",
      "name": "network",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
          "athena_properties": {},
          "catalog_id": "899076912694",
          "connection_properties": {},
          "connection_type": "NETWORK",
          "description": "",
          "id": "899076912694:eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
          "match_criteria": [],
          "name": "eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
          "physical_connection_requirements": [
            {
              "availability_zone": "eu-west-1a",
              "security_group_id_list": [
                "sg-032c47f80254c35c7",
                "sg-09096e91dd18fa7d4",
                "sg-0aa6fd5972038141a",
                "sg-0cb505f744b1c74eb"
              ],
              "subnet_id": "subnet-0a8409260cbaf999f"
            }
          ],
          "region": "eu-west-1",
          "tags": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "env",
            "Name": "job2"
          },
          "tags_all": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "env",
            "Name": "job2"
          }
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "athena_properties": true,
          "connection_properties": true,
          "match_criteria": [],
          "physical_connection_requirements": [
            {
              "security_group_id_list": [
                false,
                false,
                false,
                false
              ]
            }
          ],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_2.aws_glue_job.job",
      "module_address": "module.bb_blueprint.module.glue_job_2",
      "mode": "managed",
      "type": "aws_glue_job",
      "name": "job",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:glue:eu-west-1:899076912694:job/eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
          "command": [
            {
              "name": "glueetl",
              "python_version": "3",
              "runtime": "",
              "script_location": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/glue_jobs/src/quality.py"
            }
          ],
          "connections": [
            "eniaws-glue-euwe1-ictd-899076912694-job-l1-l2"
          ],
          "default_arguments": {
            "--continuous-log-logGroup": "/aws-glue/jobs",
            "--enable-auto-scaling": "true",
            "--enable-continuous-cloudwatch-log": "true",
            "--enable-continuous-log-filter": "true",
            "--enable-job-insights": "true",
            "--enable-metrics": "",
            "--enable-observability-metrics": "true",
            "--input_path": "",
            "--job-language": "python",
            "--output_path": ""
          },
          "description": "Glue Job",
          "execution_class": "STANDARD",
          "execution_property": [
            {
              "max_concurrent_runs": 1
            }
          ],
          "glue_version": "4.0",
          "id": "eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
          "job_mode": "SCRIPT",
          "job_run_queuing_enabled": false,
          "maintenance_window": "",
          "max_capacity": 10,
          "max_retries": 0,
          "name": "eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
          "non_overridable_arguments": {},
          "notification_property": [],
          "number_of_workers": 10,
          "region": "eu-west-1",
          "role_arn": "arn:aws:iam::899076912694:role/eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2",
          "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l1-l2",
          "source_control_details": [],
          "tags": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "env",
            "Name": "job2"
          },
          "tags_all": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "env",
            "Name": "job2"
          },
          "timeout": 2880,
          "worker_type": "G.1X"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "command": [
            {}
          ],
          "connections": [
            false
          ],
          "default_arguments": {},
          "execution_property": [
            {}
          ],
          "non_overridable_arguments": {},
          "notification_property": [],
          "source_control_details": [],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_2.aws_glue_security_configuration.this",
      "module_address": "module.bb_blueprint.module.glue_job_2",
      "mode": "managed",
      "type": "aws_glue_security_configuration",
      "name": "this",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "encryption_configuration": [
            {
              "cloudwatch_encryption": [
                {
                  "cloudwatch_encryption_mode": "SSE-KMS",
                  "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/logs"
                }
              ],
              "job_bookmarks_encryption": [
                {
                  "job_bookmarks_encryption_mode": "CSE-KMS",
                  "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/glue"
                }
              ],
              "s3_encryption": [
                {
                  "kms_key_arn": "",
                  "s3_encryption_mode": "SSE-S3"
                }
              ]
            }
          ],
          "id": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l1-l2",
          "name": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l1-l2",
          "region": "eu-west-1"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "encryption_configuration": [
            {
              "cloudwatch_encryption": [
                {}
              ],
              "job_bookmarks_encryption": [
                {}
              ],
              "s3_encryption": [
                {}
              ]
            }
          ]
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_2.aws_iam_role.role",
      "module_address": "module.bb_blueprint.module.glue_job_2",
      "mode": "managed",
      "type": "aws_iam_role",
      "name": "role",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:role/eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2",
          "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
          "create_date": "2026-02-12T09:35:19Z",
          "description": "",
          "force_detach_policies": false,
          "id": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2",
          "inline_policy": [
            {
              "name": "glue_job_permissions",
              "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"s3:PutObject\",\"s3:ListBucket\",\"s3:GetObject\",\"s3:GetBucketLocation\",\"s3:DeleteObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"S3Access\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"LogsAccess\"},{\"Action\":\"cloudwatch:PutMetricData\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"CloudWatchMetrics\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:SearchTables\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"GlueAccess\"},{\"Action\":[\"ec2:GetConnectionStatus\",\"ec2:Describe*\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"EC2Describe\"},{\"Action\":[\"ec2:DetachNetworkInterface\",\"ec2:DeleteNetworkInterface\",\"ec2:CreateNetworkInterface\",\"ec2:AttachNetworkInterface\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7\",\"arn:aws:ec2:eu-west-1:899076912694:network-interface/*\"],\"Sid\":\"EC2Modify\"},{\"Action\":[\"glue:GetConnections\",\"glue:GetConnection\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l1-l2\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueConnectionRead\"},{\"Action\":[\"ec2:DescribeVpcs\",\"ec2:DescribeVpcEndpoints\",\"ec2:DescribeSubnets\",\"ec2:DescribeSecurityGroups\",\"ec2:DescribeRouteTables\",\"ec2:DescribeNetworkInterfaces\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"EC2DescribeForGlueNetwork\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"AllowRestrictedGlueActions\"},{\"Action\":[\"logs:DisassociateKmsKey\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*\",\"arn:aws:kms:eu-west-1:899076912694:alias/aws/glue\"],\"Sid\":\"AllowCloudWatchLogsAssociateKmsKey\"}]}"
            }
          ],
          "managed_policy_arns": [],
          "max_session_duration": 3600,
          "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2",
          "name_prefix": "",
          "path": "/",
          "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
          "tags": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "Env": "env",
            "Name": "job2"
          },
          "tags_all": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "Env": "env",
            "Name": "job2"
          },
          "unique_id": "AROA5CVJI6Y3J3EVLFBB5"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "inline_policy": [
            {}
          ],
          "managed_policy_arns": [],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.glue_job_2.aws_iam_role_policy.glue_job_permissions",
      "module_address": "module.bb_blueprint.module.glue_job_2",
      "mode": "managed",
      "type": "aws_iam_role_policy",
      "name": "glue_job_permissions",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "id": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2:glue_job_permissions",
          "name": "glue_job_permissions",
          "name_prefix": "",
          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"s3:PutObject\",\"s3:ListBucket\",\"s3:GetObject\",\"s3:GetBucketLocation\",\"s3:DeleteObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"S3Access\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"LogsAccess\"},{\"Action\":\"cloudwatch:PutMetricData\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"CloudWatchMetrics\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:SearchTables\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"GlueAccess\"},{\"Action\":[\"ec2:GetConnectionStatus\",\"ec2:Describe*\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"EC2Describe\"},{\"Action\":[\"ec2:DetachNetworkInterface\",\"ec2:DeleteNetworkInterface\",\"ec2:CreateNetworkInterface\",\"ec2:AttachNetworkInterface\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7\",\"arn:aws:ec2:eu-west-1:899076912694:network-interface/*\"],\"Sid\":\"EC2Modify\"},{\"Action\":[\"glue:GetConnections\",\"glue:GetConnection\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l1-l2\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueConnectionRead\"},{\"Action\":[\"ec2:DescribeVpcs\",\"ec2:DescribeVpcEndpoints\",\"ec2:DescribeSubnets\",\"ec2:DescribeSecurityGroups\",\"ec2:DescribeRouteTables\",\"ec2:DescribeNetworkInterfaces\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"EC2DescribeForGlueNetwork\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"AllowRestrictedGlueActions\"},{\"Action\":[\"logs:DisassociateKmsKey\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*\",\"arn:aws:kms:eu-west-1:899076912694:alias/aws/glue\"],\"Sid\":\"AllowCloudWatchLogsAssociateKmsKey\"}]}",
          "role": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "glue_job_permissions",
          "role": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.lambda_trigger.aws_iam_role.role",
      "module_address": "module.bb_blueprint.module.lambda_trigger",
      "mode": "managed",
      "type": "aws_iam_role",
      "name": "role",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:role/bb-lambda-alfa-test_execution_role",
          "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"lambda.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
          "create_date": "2026-02-12T09:35:19Z",
          "description": "",
          "force_detach_policies": false,
          "id": "bb-lambda-alfa-test_execution_role",
          "inline_policy": [
            {
              "name": "lambda_permissions",
              "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:logs:*:*:*\",\"Sid\":\"AllowBasicLambdaExecution\"},{\"Action\":\"states:StartExecution\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/*\",\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"],\"Sid\":\"AllowLambdaAccessToStepFunction\"},{\"Action\":[\"s3:PutObject\",\"s3:GetObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/*\",\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"],\"Sid\":\"AllowS3InvokeLambda\"}]}"
            }
          ],
          "managed_policy_arns": [
            "arn:aws:iam::aws:policy/service-role/AWSLambdaVPCAccessExecutionRole"
          ],
          "max_session_duration": 3600,
          "name": "bb-lambda-alfa-test_execution_role",
          "name_prefix": "",
          "path": "/",
          "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
          "tags": {},
          "tags_all": {},
          "unique_id": "AROA5CVJI6Y3OUVC5LMMM"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "inline_policy": [
            {}
          ],
          "managed_policy_arns": [
            false
          ],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "bb-lambda-alfa-test_execution_role"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.lambda_trigger.aws_iam_role_policy.lambda_permissions",
      "module_address": "module.bb_blueprint.module.lambda_trigger",
      "mode": "managed",
      "type": "aws_iam_role_policy",
      "name": "lambda_permissions",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "id": "bb-lambda-alfa-test_execution_role:lambda_permissions",
          "name": "lambda_permissions",
          "name_prefix": "",
          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:logs:*:*:*\",\"Sid\":\"AllowBasicLambdaExecution\"},{\"Action\":\"states:StartExecution\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/*\",\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"],\"Sid\":\"AllowLambdaAccessToStepFunction\"},{\"Action\":[\"s3:PutObject\",\"s3:GetObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/*\",\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"],\"Sid\":\"AllowS3InvokeLambda\"}]}",
          "role": "bb-lambda-alfa-test_execution_role"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "name": "lambda_permissions",
          "role": "bb-lambda-alfa-test_execution_role"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.lambda_trigger.aws_iam_role_policy_attachment.lambda_vpc_access",
      "module_address": "module.bb_blueprint.module.lambda_trigger",
      "mode": "managed",
      "type": "aws_iam_role_policy_attachment",
      "name": "lambda_vpc_access",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "id": "bb-lambda-alfa-test_execution_role/arn:aws:iam::aws:policy/service-role/AWSLambdaVPCAccessExecutionRole",
          "policy_arn": "arn:aws:iam::aws:policy/service-role/AWSLambdaVPCAccessExecutionRole",
          "role": "bb-lambda-alfa-test_execution_role"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "policy_arn": "arn:aws:iam::aws:policy/service-role/AWSLambdaVPCAccessExecutionRole",
          "role": "bb-lambda-alfa-test_execution_role"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.lambda_trigger.aws_lambda_function.func",
      "module_address": "module.bb_blueprint.module.lambda_trigger",
      "mode": "managed",
      "type": "aws_lambda_function",
      "name": "func",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "architectures": [
            "x86_64"
          ],
          "arn": "arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
          "capacity_provider_config": [],
          "code_sha256": "wEM5Bj4bYOvtHlAqd749iee2e/+quXoveiBpRpv51/Q=",
          "code_signing_config_arn": "",
          "dead_letter_config": [],
          "description": "",
          "durable_config": [],
          "environment": [
            {
              "variables": {
                "BUCKET_L0_ID": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                "CONFIG1": "valore1",
                "CONFIG2": "valore2",
                "CONFIG3": "valore3",
                "FUNCTIONVERSION": "2db4a82d",
                "MYENV": "sd"
              }
            }
          ],
          "ephemeral_storage": [
            {
              "size": 512
            }
          ],
          "file_system_config": [],
          "filename": ".terraform/modules/bb_blueprint.lambda_trigger/lambda/function.zip",
          "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
          "handler": "pdf_to_csv.handler.lambda_handler",
          "id": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
          "image_config": [],
          "image_uri": "",
          "invoke_arn": "arn:aws:apigateway:eu-west-1:lambda:path/2015-03-31/functions/arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/invocations",
          "kms_key_arn": "",
          "last_modified": "2026-02-13T14:56:56.000+0000",
          "layers": [],
          "logging_config": [
            {
              "application_log_level": "",
              "log_format": "Text",
              "log_group": "/aws/lambda/eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
              "system_log_level": ""
            }
          ],
          "memory_size": 256,
          "package_type": "Zip",
          "publish": false,
          "publish_to": null,
          "qualified_arn": "arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test:$LATEST",
          "qualified_invoke_arn": "arn:aws:apigateway:eu-west-1:lambda:path/2015-03-31/functions/arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test:$LATEST/invocations",
          "region": "eu-west-1",
          "replace_security_groups_on_destroy": null,
          "replacement_security_group_ids": null,
          "reserved_concurrent_executions": -1,
          "response_streaming_invoke_arn": "arn:aws:apigateway:eu-west-1:lambda:path/2021-11-15/functions/arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/response-streaming-invocations",
          "role": "arn:aws:iam::899076912694:role/bb-lambda-alfa-test_execution_role",
          "runtime": "python3.12",
          "s3_bucket": null,
          "s3_key": null,
          "s3_object_version": null,
          "signing_job_arn": "",
          "signing_profile_version_arn": "",
          "skip_destroy": false,
          "snap_start": [],
          "source_code_hash": "",
          "source_code_size": 28895990,
          "source_kms_key_arn": "",
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "lambda",
            "BuildingBlockVersion": "1.0.1",
            "Env": "sd",
            "Name": "lambda"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "lambda",
            "BuildingBlockVersion": "1.0.1",
            "Env": "sd",
            "Name": "lambda"
          },
          "tenancy_config": [],
          "timeout": 3,
          "timeouts": null,
          "tracing_config": [
            {
              "mode": "Active"
            }
          ],
          "version": "$LATEST",
          "vpc_config": [
            {
              "ipv6_allowed_for_dual_stack": false,
              "security_group_ids": [
                "sg-0050539b6cdca740b"
              ],
              "subnet_ids": [
                "subnet-0bbf991ef124badcc",
                "subnet-0c4e308d22ad05ee7"
              ],
              "vpc_id": "vpc-07dd8497864cf1073"
            }
          ]
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "architectures": [
            false
          ],
          "capacity_provider_config": [],
          "dead_letter_config": [],
          "durable_config": [],
          "environment": [
            {
              "variables": {}
            }
          ],
          "ephemeral_storage": [
            {}
          ],
          "file_system_config": [],
          "image_config": [],
          "layers": [],
          "logging_config": [
            {}
          ],
          "snap_start": [],
          "tags": {},
          "tags_all": {},
          "tenancy_config": [],
          "tracing_config": [
            {}
          ],
          "vpc_config": [
            {
              "security_group_ids": [
                false
              ],
              "subnet_ids": [
                false,
                false
              ]
            }
          ]
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.lambda_trigger.aws_lambda_function_event_invoke_config.error_destination",
      "module_address": "module.bb_blueprint.module.lambda_trigger",
      "mode": "managed",
      "type": "aws_lambda_function_event_invoke_config",
      "name": "error_destination",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "destination_config": [],
          "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
          "id": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
          "maximum_event_age_in_seconds": 0,
          "maximum_retry_attempts": 2,
          "qualifier": "",
          "region": "eu-west-1"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "destination_config": []
        },
        "after_sensitive": false
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.lambda_trigger.aws_lambda_permission.resource_permission[\"eni-s3-lambda-trigger-permission-dpf-bp-dp1453\"]",
      "module_address": "module.bb_blueprint.module.lambda_trigger",
      "mode": "managed",
      "type": "aws_lambda_permission",
      "name": "resource_permission",
      "index": "eni-s3-lambda-trigger-permission-dpf-bp-dp1453",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "action": "lambda:InvokeFunction",
          "event_source_token": "",
          "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
          "function_url_auth_type": "",
          "id": "eni-s3-lambda-trigger-permission-dpf-bp-dp1453",
          "invoked_via_function_url": null,
          "principal": "s3.amazonaws.com",
          "principal_org_id": "",
          "qualifier": "",
          "region": "eu-west-1",
          "source_account": "899076912694",
          "source_arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "statement_id": "eni-s3-lambda-trigger-permission-dpf-bp-dp1453",
          "statement_id_prefix": ""
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
          "qualifier": null,
          "region": "eu-west-1",
          "statement_id": "eni-s3-lambda-trigger-permission-dpf-bp-dp1453"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.lambda_trigger.aws_security_group.lambdansg",
      "module_address": "module.bb_blueprint.module.lambda_trigger",
      "mode": "managed",
      "type": "aws_security_group",
      "name": "lambdansg",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0050539b6cdca740b",
          "description": "Security group for Lambda function",
          "egress": [],
          "id": "sg-0050539b6cdca740b",
          "ingress": [],
          "name": "bb-lambda-alfa-test_sg",
          "name_prefix": "",
          "owner_id": "899076912694",
          "region": "eu-west-1",
          "revoke_rules_on_delete": false,
          "tags": {},
          "tags_all": {},
          "timeouts": null,
          "vpc_id": "vpc-07dd8497864cf1073"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "egress": [],
          "ingress": [],
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "id": "sg-0050539b6cdca740b",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_iam_policy.iam_policy[\"0\"]",
      "module_address": "module.bb_blueprint.module.s3_buckets_artifacts",
      "mode": "managed",
      "type": "aws_iam_policy",
      "name": "iam_policy",
      "index": "0",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-artifacts",
          "attachment_count": 0,
          "delay_after_policy_creation_in_ms": null,
          "description": "",
          "id": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-artifacts",
          "name": "policy_0_dpf-bp-dp1453-artifacts",
          "name_prefix": "",
          "path": "/",
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts\"],\"Sid\":\"AllowAllS3ArtifactActions\"}],\"Version\":\"2012-10-17\"}",
          "policy_id": "ANPA5CVJI6Y3PNJ4FZDNA",
          "tags": {},
          "tags_all": {}
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-artifacts"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket",
      "module_address": "module.bb_blueprint.module.s3_buckets_artifacts",
      "mode": "managed",
      "type": "aws_s3_bucket",
      "name": "s3_bucket",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "acceleration_status": "",
          "acl": null,
          "arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "bucket_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts.s3.amazonaws.com",
          "bucket_prefix": "",
          "bucket_region": "eu-west-1",
          "bucket_regional_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts.s3.eu-west-1.amazonaws.com",
          "cors_rule": [],
          "force_destroy": true,
          "grant": [
            {
              "id": "d1feaac8a6ab06d21b99eb178e911dfdf5749f1c6a32504e3b10308ba58bfa01",
              "permissions": [
                "FULL_CONTROL"
              ],
              "type": "CanonicalUser",
              "uri": ""
            }
          ],
          "hosted_zone_id": "Z1BKCTXD74EZPE",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "lifecycle_rule": [],
          "logging": [
            {
              "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
              "target_prefix": "log/"
            }
          ],
          "object_lock_configuration": [],
          "object_lock_enabled": false,
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
          "region": "eu-west-1",
          "replication_configuration": [],
          "request_payer": "BucketOwner",
          "server_side_encryption_configuration": [
            {
              "rule": [
                {
                  "apply_server_side_encryption_by_default": [
                    {
                      "kms_master_key_id": "",
                      "sse_algorithm": "AES256"
                    }
                  ],
                  "bucket_key_enabled": false
                }
              ]
            }
          ],
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3_artifacts"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3_artifacts"
          },
          "timeouts": null,
          "versioning": [
            {
              "enabled": false,
              "mfa_delete": false
            }
          ],
          "website": [],
          "website_domain": null,
          "website_endpoint": null
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "cors_rule": [],
          "grant": [
            {
              "permissions": [
                false
              ]
            }
          ],
          "lifecycle_rule": [],
          "logging": [
            {}
          ],
          "object_lock_configuration": [],
          "replication_configuration": [],
          "server_side_encryption_configuration": [
            {
              "rule": [
                {
                  "apply_server_side_encryption_by_default": [
                    {}
                  ]
                }
              ]
            }
          ],
          "tags": {},
          "tags_all": {},
          "versioning": [
            {}
          ],
          "website": []
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket_logging.example",
      "module_address": "module.bb_blueprint.module.s3_buckets_artifacts",
      "mode": "managed",
      "type": "aws_s3_bucket_logging",
      "name": "example",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "expected_bucket_owner": "",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "region": "eu-west-1",
          "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {
                  "partition_date_source": "EventTime"
                }
              ],
              "simple_prefix": []
            }
          ],
          "target_prefix": "log/"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {}
              ],
              "simple_prefix": []
            }
          ]
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket_policy.bucket_policy",
      "module_address": "module.bb_blueprint.module.s3_buckets_artifacts",
      "mode": "managed",
      "type": "aws_s3_bucket_policy",
      "name": "bucket_policy",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
          "region": "eu-west-1"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket_public_access_block.public_access_block",
      "module_address": "module.bb_blueprint.module.s3_buckets_artifacts",
      "mode": "managed",
      "type": "aws_s3_bucket_public_access_block",
      "name": "public_access_block",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "block_public_acls": true,
          "block_public_policy": true,
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "ignore_public_acls": true,
          "region": "eu-west-1",
          "restrict_public_buckets": true,
          "skip_destroy": null
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l0.aws_iam_policy.iam_policy[\"0\"]",
      "module_address": "module.bb_blueprint.module.s3_buckets_l0",
      "mode": "managed",
      "type": "aws_iam_policy",
      "name": "iam_policy",
      "index": "0",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l0",
          "attachment_count": 0,
          "delay_after_policy_creation_in_ms": null,
          "description": "",
          "id": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l0",
          "name": "policy_0_dpf-bp-dp1453-l0",
          "name_prefix": "",
          "path": "/",
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0\"],\"Sid\":\"AllowAllS3L0Actions\"}],\"Version\":\"2012-10-17\"}",
          "policy_id": "ANPA5CVJI6Y3AHELZJF5F",
          "tags": {},
          "tags_all": {}
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l0"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket",
      "module_address": "module.bb_blueprint.module.s3_buckets_l0",
      "mode": "managed",
      "type": "aws_s3_bucket",
      "name": "s3_bucket",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "acceleration_status": "",
          "acl": null,
          "arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "bucket_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0.s3.amazonaws.com",
          "bucket_prefix": "",
          "bucket_region": "eu-west-1",
          "bucket_regional_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0.s3.eu-west-1.amazonaws.com",
          "cors_rule": [],
          "force_destroy": true,
          "grant": [
            {
              "id": "d1feaac8a6ab06d21b99eb178e911dfdf5749f1c6a32504e3b10308ba58bfa01",
              "permissions": [
                "FULL_CONTROL"
              ],
              "type": "CanonicalUser",
              "uri": ""
            }
          ],
          "hosted_zone_id": "Z1BKCTXD74EZPE",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "lifecycle_rule": [],
          "logging": [
            {
              "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
              "target_prefix": "log/"
            }
          ],
          "object_lock_configuration": [],
          "object_lock_enabled": false,
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
          "region": "eu-west-1",
          "replication_configuration": [],
          "request_payer": "BucketOwner",
          "server_side_encryption_configuration": [
            {
              "rule": [
                {
                  "apply_server_side_encryption_by_default": [
                    {
                      "kms_master_key_id": "",
                      "sse_algorithm": "AES256"
                    }
                  ],
                  "bucket_key_enabled": false
                }
              ]
            }
          ],
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3_l0"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3_l0"
          },
          "timeouts": null,
          "versioning": [
            {
              "enabled": false,
              "mfa_delete": false
            }
          ],
          "website": [],
          "website_domain": null,
          "website_endpoint": null
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "cors_rule": [],
          "grant": [
            {
              "permissions": [
                false
              ]
            }
          ],
          "lifecycle_rule": [],
          "logging": [
            {}
          ],
          "object_lock_configuration": [],
          "replication_configuration": [],
          "server_side_encryption_configuration": [
            {
              "rule": [
                {
                  "apply_server_side_encryption_by_default": [
                    {}
                  ]
                }
              ]
            }
          ],
          "tags": {},
          "tags_all": {},
          "versioning": [
            {}
          ],
          "website": []
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket_logging.example",
      "module_address": "module.bb_blueprint.module.s3_buckets_l0",
      "mode": "managed",
      "type": "aws_s3_bucket_logging",
      "name": "example",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "expected_bucket_owner": "",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "region": "eu-west-1",
          "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {
                  "partition_date_source": "EventTime"
                }
              ],
              "simple_prefix": []
            }
          ],
          "target_prefix": "log/"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {}
              ],
              "simple_prefix": []
            }
          ]
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket_policy.bucket_policy",
      "module_address": "module.bb_blueprint.module.s3_buckets_l0",
      "mode": "managed",
      "type": "aws_s3_bucket_policy",
      "name": "bucket_policy",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
          "region": "eu-west-1"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket_public_access_block.public_access_block",
      "module_address": "module.bb_blueprint.module.s3_buckets_l0",
      "mode": "managed",
      "type": "aws_s3_bucket_public_access_block",
      "name": "public_access_block",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "block_public_acls": true,
          "block_public_policy": true,
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "ignore_public_acls": true,
          "region": "eu-west-1",
          "restrict_public_buckets": true,
          "skip_destroy": null
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l1.aws_iam_policy.iam_policy[\"0\"]",
      "module_address": "module.bb_blueprint.module.s3_buckets_l1",
      "mode": "managed",
      "type": "aws_iam_policy",
      "name": "iam_policy",
      "index": "0",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l1",
          "attachment_count": 0,
          "delay_after_policy_creation_in_ms": null,
          "description": "",
          "id": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l1",
          "name": "policy_0_dpf-bp-dp1453-l1",
          "name_prefix": "",
          "path": "/",
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l1\"],\"Sid\":\"AllowAllS3L1Actions\"}],\"Version\":\"2012-10-17\"}",
          "policy_id": "ANPA5CVJI6Y3FWMV62TFZ",
          "tags": {},
          "tags_all": {}
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket.s3_bucket",
      "module_address": "module.bb_blueprint.module.s3_buckets_l1",
      "mode": "managed",
      "type": "aws_s3_bucket",
      "name": "s3_bucket",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "acceleration_status": "",
          "acl": null,
          "arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "bucket_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1.s3.amazonaws.com",
          "bucket_prefix": "",
          "bucket_region": "eu-west-1",
          "bucket_regional_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1.s3.eu-west-1.amazonaws.com",
          "cors_rule": [],
          "force_destroy": true,
          "grant": [
            {
              "id": "d1feaac8a6ab06d21b99eb178e911dfdf5749f1c6a32504e3b10308ba58bfa01",
              "permissions": [
                "FULL_CONTROL"
              ],
              "type": "CanonicalUser",
              "uri": ""
            }
          ],
          "hosted_zone_id": "Z1BKCTXD74EZPE",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "lifecycle_rule": [],
          "logging": [
            {
              "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
              "target_prefix": "log/"
            }
          ],
          "object_lock_configuration": [],
          "object_lock_enabled": false,
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
          "region": "eu-west-1",
          "replication_configuration": [],
          "request_payer": "BucketOwner",
          "server_side_encryption_configuration": [
            {
              "rule": [
                {
                  "apply_server_side_encryption_by_default": [
                    {
                      "kms_master_key_id": "",
                      "sse_algorithm": "AES256"
                    }
                  ],
                  "bucket_key_enabled": false
                }
              ]
            }
          ],
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3_l1"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3_l1"
          },
          "timeouts": null,
          "versioning": [
            {
              "enabled": false,
              "mfa_delete": false
            }
          ],
          "website": [],
          "website_domain": null,
          "website_endpoint": null
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "cors_rule": [],
          "grant": [
            {
              "permissions": [
                false
              ]
            }
          ],
          "lifecycle_rule": [],
          "logging": [
            {}
          ],
          "object_lock_configuration": [],
          "replication_configuration": [],
          "server_side_encryption_configuration": [
            {
              "rule": [
                {
                  "apply_server_side_encryption_by_default": [
                    {}
                  ]
                }
              ]
            }
          ],
          "tags": {},
          "tags_all": {},
          "versioning": [
            {}
          ],
          "website": []
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket_logging.example",
      "module_address": "module.bb_blueprint.module.s3_buckets_l1",
      "mode": "managed",
      "type": "aws_s3_bucket_logging",
      "name": "example",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "expected_bucket_owner": "",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "region": "eu-west-1",
          "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {
                  "partition_date_source": "EventTime"
                }
              ],
              "simple_prefix": []
            }
          ],
          "target_prefix": "log/"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {}
              ],
              "simple_prefix": []
            }
          ]
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket_policy.bucket_policy",
      "module_address": "module.bb_blueprint.module.s3_buckets_l1",
      "mode": "managed",
      "type": "aws_s3_bucket_policy",
      "name": "bucket_policy",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
          "region": "eu-west-1"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket_public_access_block.public_access_block",
      "module_address": "module.bb_blueprint.module.s3_buckets_l1",
      "mode": "managed",
      "type": "aws_s3_bucket_public_access_block",
      "name": "public_access_block",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "block_public_acls": true,
          "block_public_policy": true,
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "ignore_public_acls": true,
          "region": "eu-west-1",
          "restrict_public_buckets": true,
          "skip_destroy": null
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l2.aws_iam_policy.iam_policy[\"0\"]",
      "module_address": "module.bb_blueprint.module.s3_buckets_l2",
      "mode": "managed",
      "type": "aws_iam_policy",
      "name": "iam_policy",
      "index": "0",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l2",
          "attachment_count": 0,
          "delay_after_policy_creation_in_ms": null,
          "description": "",
          "id": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l2",
          "name": "policy_0_dpf-bp-dp1453-l2",
          "name_prefix": "",
          "path": "/",
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l1\"],\"Sid\":\"AllowAllS3L2Actions\"}],\"Version\":\"2012-10-17\"}",
          "policy_id": "ANPA5CVJI6Y3MI4AZWR42",
          "tags": {},
          "tags_all": {}
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "tags": {},
          "tags_all": {}
        },
        "after_sensitive": false,
        "before_identity": {
          "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l2"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket.s3_bucket",
      "module_address": "module.bb_blueprint.module.s3_buckets_l2",
      "mode": "managed",
      "type": "aws_s3_bucket",
      "name": "s3_bucket",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "acceleration_status": "",
          "acl": null,
          "arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "bucket_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2.s3.amazonaws.com",
          "bucket_prefix": "",
          "bucket_region": "eu-west-1",
          "bucket_regional_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2.s3.eu-west-1.amazonaws.com",
          "cors_rule": [],
          "force_destroy": true,
          "grant": [
            {
              "id": "d1feaac8a6ab06d21b99eb178e911dfdf5749f1c6a32504e3b10308ba58bfa01",
              "permissions": [
                "FULL_CONTROL"
              ],
              "type": "CanonicalUser",
              "uri": ""
            }
          ],
          "hosted_zone_id": "Z1BKCTXD74EZPE",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "lifecycle_rule": [],
          "logging": [
            {
              "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
              "target_prefix": "log/"
            }
          ],
          "object_lock_configuration": [],
          "object_lock_enabled": false,
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
          "region": "eu-west-1",
          "replication_configuration": [],
          "request_payer": "BucketOwner",
          "server_side_encryption_configuration": [
            {
              "rule": [
                {
                  "apply_server_side_encryption_by_default": [
                    {
                      "kms_master_key_id": "",
                      "sse_algorithm": "AES256"
                    }
                  ],
                  "bucket_key_enabled": false
                }
              ]
            }
          ],
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3_l2"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3_l2"
          },
          "timeouts": null,
          "versioning": [
            {
              "enabled": false,
              "mfa_delete": false
            }
          ],
          "website": [],
          "website_domain": null,
          "website_endpoint": null
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "cors_rule": [],
          "grant": [
            {
              "permissions": [
                false
              ]
            }
          ],
          "lifecycle_rule": [],
          "logging": [
            {}
          ],
          "object_lock_configuration": [],
          "replication_configuration": [],
          "server_side_encryption_configuration": [
            {
              "rule": [
                {
                  "apply_server_side_encryption_by_default": [
                    {}
                  ]
                }
              ]
            }
          ],
          "tags": {},
          "tags_all": {},
          "versioning": [
            {}
          ],
          "website": []
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket_logging.example",
      "module_address": "module.bb_blueprint.module.s3_buckets_l2",
      "mode": "managed",
      "type": "aws_s3_bucket_logging",
      "name": "example",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "expected_bucket_owner": "",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "region": "eu-west-1",
          "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {
                  "partition_date_source": "EventTime"
                }
              ],
              "simple_prefix": []
            }
          ],
          "target_prefix": "log/"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {}
              ],
              "simple_prefix": []
            }
          ]
        },
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket_policy.bucket_policy",
      "module_address": "module.bb_blueprint.module.s3_buckets_l2",
      "mode": "managed",
      "type": "aws_s3_bucket_policy",
      "name": "bucket_policy",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
          "region": "eu-west-1"
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket_public_access_block.public_access_block",
      "module_address": "module.bb_blueprint.module.s3_buckets_l2",
      "mode": "managed",
      "type": "aws_s3_bucket_public_access_block",
      "name": "public_access_block",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "delete"
        ],
        "before": {
          "block_public_acls": true,
          "block_public_policy": true,
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "ignore_public_acls": true,
          "region": "eu-west-1",
          "restrict_public_buckets": true,
          "skip_destroy": null
        },
        "after": null,
        "after_unknown": {},
        "before_sensitive": {},
        "after_sensitive": false,
        "before_identity": {
          "account_id": "899076912694",
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
          "region": "eu-west-1"
        }
      },
      "action_reason": "delete_because_no_resource_config"
    },
    {
      "address": "module.blueprint.module.glue_catalog_database[\"raw_db\"].aws_glue_catalog_database.catalog",
      "module_address": "module.blueprint.module.glue_catalog_database[\"raw_db\"]",
      "mode": "managed",
      "type": "aws_glue_catalog_database",
      "name": "catalog",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "description": "Glue database per i dati raw",
          "federated_database": [],
          "name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
          "parameters": null,
          "region": "eu-west-1",
          "tags": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "Env": "sd"
          },
          "tags_all": {
            "ApplicationID": "id",
            "ApplicationName": "test",
            "Env": "sd"
          },
          "target_database": []
        },
        "after_unknown": {
          "arn": true,
          "catalog_id": true,
          "create_table_default_permission": true,
          "federated_database": [],
          "id": true,
          "location_uri": true,
          "tags": {},
          "tags_all": {},
          "target_database": []
        },
        "before_sensitive": false,
        "after_sensitive": {
          "create_table_default_permission": [],
          "federated_database": [],
          "tags": {},
          "tags_all": {},
          "target_database": []
        }
      }
    },
    {
      "address": "module.blueprint.module.glue_catalog_database[\"raw_db\"].aws_iam_policy.iam_policy[\"0\"]",
      "module_address": "module.blueprint.module.glue_catalog_database[\"raw_db\"]",
      "mode": "managed",
      "type": "aws_iam_policy",
      "name": "iam_policy",
      "index": "0",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "delay_after_policy_creation_in_ms": null,
          "description": null,
          "name": "policy_glue_db_0_raw",
          "path": "/",
          "policy": "{\"Statement\":[{\"Action\":[\"glue:GetTables\",\"glue:GetDatabase\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/raw_db/*\",\"arn:aws:glue:eu-west-1:899076912694:database/raw_db\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueDatabaseRead\"}],\"Version\":\"2012-10-17\"}",
          "tags": null
        },
        "after_unknown": {
          "arn": true,
          "attachment_count": true,
          "id": true,
          "name_prefix": true,
          "policy_id": true,
          "tags_all": true
        },
        "before_sensitive": false,
        "after_sensitive": {
          "tags_all": {}
        },
        "after_identity": {
          "arn": null
        }
      }
    },
    {
      "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_glue_crawler.crawler",
      "module_address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"]",
      "mode": "managed",
      "type": "aws_glue_crawler",
      "name": "crawler",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "catalog_target": [],
          "classifiers": null,
          "configuration": null,
          "database_name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
          "delta_target": [],
          "description": null,
          "dynamodb_target": [],
          "hudi_target": [],
          "iceberg_target": [],
          "jdbc_target": [],
          "lake_formation_configuration": [],
          "lineage_configuration": [],
          "mongodb_target": [],
          "name": "eniaws-glue-crw-euwe1-ictd-899076912694-bp1.0.0",
          "recrawl_policy": [],
          "region": "eu-west-1",
          "s3_target": [
            {
              "connection_name": null,
              "dlq_event_queue_arn": null,
              "event_queue_arn": null,
              "exclusions": null,
              "path": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw/",
              "sample_size": null
            }
          ],
          "schedule": null,
          "schema_change_policy": [],
          "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp",
          "table_prefix": null,
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd"
          }
        },
        "after_unknown": {
          "arn": true,
          "catalog_target": [],
          "delta_target": [],
          "dynamodb_target": [],
          "hudi_target": [],
          "iceberg_target": [],
          "id": true,
          "jdbc_target": [],
          "lake_formation_configuration": [],
          "lineage_configuration": [],
          "mongodb_target": [],
          "recrawl_policy": [],
          "role": true,
          "s3_target": [
            {}
          ],
          "schema_change_policy": [],
          "tags": {},
          "tags_all": {}
        },
        "before_sensitive": false,
        "after_sensitive": {
          "catalog_target": [],
          "delta_target": [],
          "dynamodb_target": [],
          "hudi_target": [],
          "iceberg_target": [],
          "jdbc_target": [],
          "lake_formation_configuration": [],
          "lineage_configuration": [],
          "mongodb_target": [],
          "recrawl_policy": [],
          "s3_target": [
            {}
          ],
          "schema_change_policy": [],
          "tags": {},
          "tags_all": {}
        }
      }
    },
    {
      "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_iam_role.role",
      "module_address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"]",
      "mode": "managed",
      "type": "aws_iam_role",
      "name": "role",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
          "description": null,
          "force_detach_policies": false,
          "max_session_duration": 3600,
          "name": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-bp1.0.0",
          "path": "/",
          "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd"
          }
        },
        "after_unknown": {
          "arn": true,
          "create_date": true,
          "id": true,
          "inline_policy": true,
          "managed_policy_arns": true,
          "name_prefix": true,
          "tags": {},
          "tags_all": {},
          "unique_id": true
        },
        "before_sensitive": false,
        "after_sensitive": {
          "inline_policy": [],
          "managed_policy_arns": [],
          "tags": {},
          "tags_all": {}
        },
        "after_identity": {
          "account_id": null,
          "name": null
        }
      }
    },
    {
      "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_iam_role_policy.glue_crawler_permissions",
      "module_address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"]",
      "mode": "managed",
      "type": "aws_iam_role_policy",
      "name": "glue_crawler_permissions",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "name": "glue_crawler_permissions",
          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":\"s3:ListBucket\",\"Condition\":{\"StringLike\":{\"s3:prefix\":[\"raw//*\",\"raw/\"]}},\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0\",\"Sid\":\"S3ListBucket\"},{\"Action\":\"s3:GetObject\",\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw//*\",\"Sid\":\"S3ReadObjects\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:GetTables\",\"glue:GetTable\",\"glue:GetDatabases\",\"glue:GetDatabase\",\"glue:CreateTable\",\"glue:CreatePartition\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueCatalogDbTableAccess\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"],\"Sid\":\"GlueCrawlerLogs\"},{\"Action\":\"glue:GetSecurityConfiguration\",\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:security-configuration/eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp\",\"Sid\":\"GlueSecurityConfigurationAccess\"}]}"
        },
        "after_unknown": {
          "id": true,
          "name_prefix": true,
          "role": true
        },
        "before_sensitive": false,
        "after_sensitive": {},
        "after_identity": {
          "account_id": null,
          "name": null,
          "role": null
        }
      }
    },
    {
      "address": "module.blueprint.module.glue_job.data.aws_iam_policy_document.glue_job_combined_policy",
      "module_address": "module.blueprint.module.glue_job",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "glue_job_combined_policy",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": [
            null,
            "{\n  \"Version\": \"2012-10-17\",\n  \"Statement\": [\n    {\n      \"Sid\": \"AllowRestrictedGlueActions\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"glue:UpdateTable\",\n        \"glue:UpdatePartition\",\n        \"glue:UpdateJob\",\n        \"glue:StartJobRun\",\n        \"glue:GetTable\",\n        \"glue:GetPartition\",\n        \"glue:GetJobRun\",\n        \"glue:GetJob\",\n        \"glue:GetDatabase\",\n        \"glue:BatchUpdatePartition\",\n        \"glue:BatchStopJobRun\",\n        \"glue:BatchGetPartition\",\n        \"glue:BatchCreatePartition\"\n      ],\n      \"Resource\": \"arn:aws:glue:eu-west-1:899076912694:*\"\n    }\n  ]\n}"
          ],
          "statement": [],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "source_policy_documents": [
            true,
            false
          ],
          "statement": []
        },
        "before_sensitive": false,
        "after_sensitive": {
          "source_policy_documents": [
            false,
            false
          ],
          "statement": []
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.glue_job.data.aws_iam_policy_document.glue_job_policy",
      "module_address": "module.blueprint.module.glue_job",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "glue_job_policy",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": null,
          "statement": [
            {
              "actions": [
                "s3:DeleteObject",
                "s3:GetBucketLocation",
                "s3:GetObject",
                "s3:ListBucket",
                "s3:PutObject"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [],
              "resources": [
                null,
                null
              ],
              "sid": "S3Access"
            },
            {
              "actions": [
                "logs:CreateLogGroup",
                "logs:CreateLogStream",
                "logs:DescribeLogGroups",
                "logs:PutLogEvents"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [],
              "resources": [
                "arn:aws:logs:*:*:log-group:/aws-glue/*",
                "arn:aws:logs:*:*:log-group:/aws-glue/*:*"
              ],
              "sid": "LogsAccess"
            },
            {
              "actions": [
                "cloudwatch:PutMetricData"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [],
              "resources": [
                "*"
              ],
              "sid": "CloudWatchMetrics"
            },
            {
              "actions": [
                "glue:BatchCreatePartition",
                "glue:BatchGetPartition",
                "glue:BatchStopJobRun",
                "glue:BatchUpdatePartition",
                "glue:GetDatabase",
                "glue:GetJob",
                "glue:GetJobRun",
                "glue:GetPartition",
                "glue:GetTable",
                "glue:StartJobRun",
                "glue:UpdateJob",
                "glue:UpdatePartition",
                "glue:UpdateTable"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [],
              "resources": [
                "arn:aws:glue:eu-west-1:899076912694:*"
              ],
              "sid": "GlueAccess"
            },
            {
              "actions": [
                "ec2:AttachNetworkInterface",
                "ec2:CreateNetworkInterface",
                "ec2:DeleteNetworkInterface",
                "ec2:DetachNetworkInterface"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [],
              "resources": [
                "arn:aws:ec2:eu-west-1:899076912694:network-interface/*",
                "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7",
                "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4",
                "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a",
                "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb",
                "arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f"
              ],
              "sid": "EC2Modify"
            }
          ],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "statement": [
            {
              "actions": [
                false,
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                true,
                true
              ]
            },
            {
              "actions": [
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false,
                false
              ]
            },
            {
              "actions": [
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false,
                false,
                false,
                false,
                false,
                false
              ]
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "statement": [
            {
              "actions": [
                false,
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false,
                false
              ]
            },
            {
              "actions": [
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false,
                false
              ]
            },
            {
              "actions": [
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false,
                false,
                false,
                false,
                false,
                false
              ]
            }
          ]
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.glue_job.data.aws_iam_policy_document.glue_resource_policy_doc",
      "module_address": "module.blueprint.module.glue_job",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "glue_resource_policy_doc",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": null,
          "statement": [
            {
              "actions": [
                "glue:*"
              ],
              "condition": [
                {
                  "test": "StringEquals",
                  "values": [
                    "638883080465"
                  ],
                  "variable": "aws:VpceAccount"
                }
              ],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "*"
                  ],
                  "type": "*"
                }
              ],
              "resources": [
                "arn:aws:glue:eu-west-1:899076912694:*"
              ],
              "sid": "AllowActionsFromInsideVPC"
            },
            {
              "actions": [
                "glue:BatchGet*",
                "glue:Get*",
                "glue:List*"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                  ],
                  "type": "AWS"
                }
              ],
              "resources": [
                "arn:aws:glue:eu-west-1:899076912694:*"
              ],
              "sid": "AllowPrisma"
            },
            {
              "actions": [
                "glue:BatchGet*",
                "glue:Get*",
                "glue:List*"
              ],
              "condition": [
                {
                  "test": "IpAddress",
                  "values": [
                    "10.68.98.160/27",
                    "10.68.98.128/27"
                  ],
                  "variable": "aws:VpcSourceIp"
                },
                {
                  "test": "StringEquals",
                  "values": [
                    "vpc-0fbd9e814ef60d4ac"
                  ],
                  "variable": "aws:SourceVpc"
                }
              ],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "*"
                  ],
                  "type": "*"
                }
              ],
              "resources": [
                "arn:aws:glue:eu-west-1:899076912694:*"
              ],
              "sid": "AllowPublicThroughF5"
            },
            {
              "actions": [
                "glue:*"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "arn:aws:iam::209923409268:role/AWSAFTExecution",
                    "arn:aws:iam::468861045281:role/AWSAFTExecution"
                  ],
                  "type": "AWS"
                }
              ],
              "resources": [
                "arn:aws:glue:eu-west-1:899076912694:*"
              ],
              "sid": "AllowAFTExecution"
            },
            {
              "actions": null,
              "condition": [
                {
                  "test": "BoolIfExists",
                  "values": [
                    "false"
                  ],
                  "variable": "aws:PrincipalIsAWSService"
                },
                {
                  "test": "NotIpAddress",
                  "values": [
                    "10.68.98.160/27",
                    "10.68.98.128/27"
                  ],
                  "variable": "aws:VpcSourceIp"
                },
                {
                  "test": "StringNotEquals",
                  "variable": "aws:PrincipalArn"
                },
                {
                  "test": "StringNotEquals",
                  "values": [
                    "638883080465"
                  ],
                  "variable": "aws:VpceAccount"
                }
              ],
              "effect": "Deny",
              "not_actions": [
                "glue:BatchGet*",
                "glue:DeleteResourcePolicy",
                "glue:Get*",
                "glue:GetResourcePolicy",
                "glue:List*",
                "glue:PutResourcePolicy"
              ],
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "*"
                  ],
                  "type": "AWS"
                }
              ],
              "resources": [
                "arn:aws:glue:eu-west-1:899076912694:*"
              ],
              "sid": "DenyNotPrincipals"
            },
            {
              "actions": [
                "glue:*"
              ],
              "condition": [
                {
                  "test": "Bool",
                  "values": [
                    "false"
                  ],
                  "variable": "aws:SecureTransport"
                }
              ],
              "effect": "Deny",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "*"
                  ],
                  "type": "*"
                }
              ],
              "resources": [
                "arn:aws:glue:eu-west-1:899076912694:*"
              ],
              "sid": "DenyNonHTTPS"
            }
          ],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false,
                false,
                false
              ],
              "condition": [
                {
                  "values": [
                    false,
                    false
                  ]
                },
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false,
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "condition": [
                {
                  "values": [
                    false
                  ]
                },
                {
                  "values": [
                    false,
                    false
                  ]
                },
                {
                  "values": true
                },
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_actions": [
                false,
                false,
                false,
                false,
                false,
                false
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false,
                false,
                false
              ],
              "condition": [
                {
                  "values": [
                    false,
                    false
                  ]
                },
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false,
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "condition": [
                {
                  "values": [
                    false
                  ]
                },
                {
                  "values": [
                    false,
                    false
                  ]
                },
                {
                  "values": []
                },
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_actions": [
                false,
                false,
                false,
                false,
                false,
                false
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            },
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            }
          ]
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.glue_job.aws_glue_job.job",
      "module_address": "module.blueprint.module.glue_job",
      "mode": "managed",
      "type": "aws_glue_job",
      "name": "job",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "command": [
            {
              "name": "glueetl",
              "python_version": "3"
            }
          ],
          "connections": null,
          "default_arguments": {
            "--continuous-log-logGroup": "/aws-glue/jobs",
            "--enable-auto-scaling": "true",
            "--enable-continuous-cloudwatch-log": "true",
            "--enable-continuous-log-filter": "true",
            "--enable-metrics": "",
            "--job-language": "python"
          },
          "description": "Glue ETL job",
          "execution_class": "STANDARD",
          "execution_property": [
            {
              "max_concurrent_runs": 1
            }
          ],
          "glue_version": "5.0",
          "job_run_queuing_enabled": null,
          "maintenance_window": null,
          "max_retries": 1,
          "name": "eniaws-glue-euwe1-ictd-899076912694-dpf-bp",
          "non_overridable_arguments": null,
          "notification_property": [
            {
              "notify_delay_after": 3
            }
          ],
          "number_of_workers": 2,
          "region": "eu-west-1",
          "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp",
          "source_control_details": [],
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "sd",
            "Name": "glue"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "aws_glue",
            "BuildingBlockVersion": "0.0.0",
            "Env": "sd",
            "Name": "glue"
          },
          "timeout": 2880,
          "worker_type": "G.1X"
        },
        "after_unknown": {
          "arn": true,
          "command": [
            {
              "runtime": true,
              "script_location": true
            }
          ],
          "default_arguments": {},
          "execution_property": [
            {}
          ],
          "id": true,
          "job_mode": true,
          "max_capacity": true,
          "notification_property": [
            {}
          ],
          "role_arn": true,
          "source_control_details": [],
          "tags": {},
          "tags_all": {}
        },
        "before_sensitive": false,
        "after_sensitive": {
          "command": [
            {}
          ],
          "default_arguments": {},
          "execution_property": [
            {}
          ],
          "notification_property": [
            {}
          ],
          "source_control_details": [],
          "tags": {},
          "tags_all": {}
        }
      }
    },
    {
      "address": "module.blueprint.module.glue_job.aws_glue_resource_policy.this",
      "module_address": "module.blueprint.module.glue_job",
      "mode": "managed",
      "type": "aws_glue_resource_policy",
      "name": "this",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "enable_hybrid": "TRUE",
          "region": "eu-west-1"
        },
        "after_unknown": {
          "id": true,
          "policy": true
        },
        "before_sensitive": false,
        "after_sensitive": {},
        "after_identity": {
          "account_id": null,
          "region": null
        }
      }
    },
    {
      "address": "module.blueprint.module.glue_job.aws_glue_security_configuration.this",
      "module_address": "module.blueprint.module.glue_job",
      "mode": "managed",
      "type": "aws_glue_security_configuration",
      "name": "this",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "encryption_configuration": [
            {
              "cloudwatch_encryption": [
                {
                  "cloudwatch_encryption_mode": "SSE-KMS",
                  "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/glue"
                }
              ],
              "job_bookmarks_encryption": [
                {
                  "job_bookmarks_encryption_mode": "CSE-KMS",
                  "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/glue"
                }
              ],
              "s3_encryption": [
                {
                  "kms_key_arn": null,
                  "s3_encryption_mode": "SSE-S3"
                }
              ]
            }
          ],
          "name": "eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp",
          "region": "eu-west-1"
        },
        "after_unknown": {
          "encryption_configuration": [
            {
              "cloudwatch_encryption": [
                {}
              ],
              "job_bookmarks_encryption": [
                {}
              ],
              "s3_encryption": [
                {}
              ]
            }
          ],
          "id": true
        },
        "before_sensitive": false,
        "after_sensitive": {
          "encryption_configuration": [
            {
              "cloudwatch_encryption": [
                {}
              ],
              "job_bookmarks_encryption": [
                {}
              ],
              "s3_encryption": [
                {}
              ]
            }
          ]
        }
      }
    },
    {
      "address": "module.blueprint.module.glue_job.aws_iam_role.role",
      "module_address": "module.blueprint.module.glue_job",
      "mode": "managed",
      "type": "aws_iam_role",
      "name": "role",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
          "description": null,
          "force_detach_policies": false,
          "max_session_duration": 3600,
          "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-dpf-bp",
          "path": "/",
          "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd",
            "Name": "glue"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "Env": "sd",
            "Name": "glue"
          }
        },
        "after_unknown": {
          "arn": true,
          "create_date": true,
          "id": true,
          "inline_policy": true,
          "managed_policy_arns": true,
          "name_prefix": true,
          "tags": {},
          "tags_all": {},
          "unique_id": true
        },
        "before_sensitive": false,
        "after_sensitive": {
          "inline_policy": [],
          "managed_policy_arns": [],
          "tags": {},
          "tags_all": {}
        },
        "after_identity": {
          "account_id": null,
          "name": null
        }
      }
    },
    {
      "address": "module.blueprint.module.glue_job.aws_iam_role_policy.glue_job_permissions",
      "module_address": "module.blueprint.module.glue_job",
      "mode": "managed",
      "type": "aws_iam_role_policy",
      "name": "glue_job_permissions",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "name": "glue_job_permissions"
        },
        "after_unknown": {
          "id": true,
          "name_prefix": true,
          "policy": true,
          "role": true
        },
        "before_sensitive": false,
        "after_sensitive": {},
        "after_identity": {
          "account_id": null,
          "name": null,
          "role": null
        }
      }
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_prisma",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "allow_prisma",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": null,
          "statement": [
            {
              "actions": [
                "s3:GetAccelerateConfiguration",
                "s3:GetAnalyticsConfiguration",
                "s3:GetBucket*",
                "s3:GetBucketAcl",
                "s3:GetBucketCORS",
                "s3:GetBucketLocation",
                "s3:GetBucketLogging",
                "s3:GetBucketObjectLockConfiguration",
                "s3:GetBucketOwnershipControls",
                "s3:GetBucketPolicy",
                "s3:GetBucketPolicyStatus",
                "s3:GetBucketPublicAccessBlock",
                "s3:GetBucketTagging",
                "s3:GetBucketVersioning",
                "s3:GetBucketWebsite",
                "s3:GetEncryptionConfiguration",
                "s3:GetInventoryConfiguration",
                "s3:GetLifecycleConfiguration",
                "s3:GetMetricsConfiguration",
                "s3:GetReplicationConfiguration",
                "s3:ListBucket"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                  ],
                  "type": "AWS"
                }
              ],
              "resources": [
                null
              ],
              "sid": "AllowPrisma"
            }
          ],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "statement": [
            {
              "actions": [
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                true
              ]
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "statement": [
            {
              "actions": [
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            }
          ]
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_prisma_object",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "allow_prisma_object",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": null,
          "statement": [
            {
              "actions": [
                "s3:GetObjectAcl",
                "s3:GetObjectTagging",
                "s3:GetObjectVersionAcl"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                  ],
                  "type": "AWS"
                }
              ],
              "resources": [
                null
              ],
              "sid": "AllowPrismaObject"
            }
          ],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "statement": [
            {
              "actions": [
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                true
              ]
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "statement": [
            {
              "actions": [
                false,
                false,
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false
              ]
            }
          ]
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_public_through_f5",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "allow_public_through_f5",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": null,
          "statement": [
            {
              "actions": [
                "s3:GetObject"
              ],
              "condition": [
                {
                  "test": "IpAddress",
                  "values": [
                    "10.68.98.160/27",
                    "10.68.98.128/27"
                  ],
                  "variable": "aws:VpcSourceIp"
                },
                {
                  "test": "StringEquals",
                  "values": [
                    "vpc-0fbd9e814ef60d4ac"
                  ],
                  "variable": "aws:SourceVpc"
                }
              ],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "*"
                  ],
                  "type": "*"
                }
              ],
              "resources": [
                null,
                null
              ],
              "sid": "AllowPublicThroughF5"
            }
          ],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false,
                    false
                  ]
                },
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                true,
                true
              ]
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false,
                    false
                  ]
                },
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false,
                false
              ]
            }
          ]
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_ssl_only",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "allow_ssl_only",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": null,
          "statement": [
            {
              "actions": [
                "s3:*"
              ],
              "condition": [
                {
                  "test": "Bool",
                  "values": [
                    "false"
                  ],
                  "variable": "aws:SecureTransport"
                }
              ],
              "effect": "Deny",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "*"
                  ],
                  "type": "*"
                }
              ],
              "resources": [
                null,
                null
              ],
              "sid": "AllowSSLOnly"
            }
          ],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                true,
                true
              ]
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false,
                false
              ]
            }
          ]
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_vpc_source",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "allow_vpc_source",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": null,
          "statement": [
            {
              "actions": [
                "s3:*"
              ],
              "condition": [
                {
                  "test": "StringEquals",
                  "values": [
                    "638883080465"
                  ],
                  "variable": "aws:VpceAccount"
                }
              ],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [
                {
                  "identifiers": [
                    "*"
                  ],
                  "type": "*"
                }
              ],
              "resources": [
                null,
                null
              ],
              "sid": "AllowActionsFromInsideVPC"
            }
          ],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                true,
                true
              ]
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [],
              "principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "resources": [
                false,
                false
              ]
            }
          ]
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.combined",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "combined",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "statement": [],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "source_policy_documents": true,
          "statement": []
        },
        "before_sensitive": false,
        "after_sensitive": {
          "source_policy_documents": [],
          "statement": []
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.custom_iam_policy_document[\"0\"]",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "custom_iam_policy_document",
      "index": "0",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": null,
          "statement": [
            {
              "actions": [
                "s3:*"
              ],
              "condition": [],
              "effect": "Allow",
              "not_actions": null,
              "not_principals": [],
              "not_resources": null,
              "principals": [],
              "resources": [
                "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts",
                "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts/*"
              ],
              "sid": "AllowAllS3Actions"
            }
          ],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false,
                false
              ]
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [],
              "not_principals": [],
              "principals": [],
              "resources": [
                false,
                false
              ]
            }
          ]
        }
      },
      "action_reason": "read_because_dependency_pending"
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.deny_not_principals",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "data",
      "type": "aws_iam_policy_document",
      "name": "deny_not_principals",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "read"
        ],
        "before": null,
        "after": {
          "override_json": null,
          "override_policy_documents": null,
          "policy_id": null,
          "source_json": null,
          "source_policy_documents": null,
          "statement": [
            {
              "actions": [
                "s3:*"
              ],
              "condition": [
                {
                  "test": "BoolIfExists",
                  "values": [
                    "false"
                  ],
                  "variable": "aws:PrincipalIsAWSService"
                },
                {
                  "test": "NotIpAddress",
                  "values": [
                    "10.68.98.160/27",
                    "10.68.98.128/27"
                  ],
                  "variable": "aws:VpcSourceIp"
                },
                {
                  "test": "StringNotEquals",
                  "values": [
                    "638883080465"
                  ],
                  "variable": "aws:VpceAccount"
                },
                {
                  "test": "StringNotEquals",
                  "values": [
                    "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                  ],
                  "variable": "aws:PrincipalArn"
                }
              ],
              "effect": "Deny",
              "not_actions": null,
              "not_principals": [
                {
                  "identifiers": [
                    "arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member"
                  ],
                  "type": "AWS"
                }
              ],
              "not_resources": null,
              "principals": [],
              "resources": [
                null,
                null
              ],
              "sid": "DenyNotPrincipals"
            }
          ],
          "version": null
        },
        "after_unknown": {
          "id": true,
          "json": true,
          "minified_json": true,
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                },
                {
                  "values": [
                    false,
                    false
                  ]
                },
                {
                  "values": [
                    false
                  ]
                },
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "principals": [],
              "resources": [
                true,
                true
              ]
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "statement": [
            {
              "actions": [
                false
              ],
              "condition": [
                {
                  "values": [
                    false
                  ]
                },
                {
                  "values": [
                    false,
                    false
                  ]
                },
                {
                  "values": [
                    false
                  ]
                },
                {
                  "values": [
                    false
                  ]
                }
              ],
              "not_principals": [
                {
                  "identifiers": [
                    false
                  ]
                }
              ],
              "principals": [],
              "resources": [
                false,
                false
              ]
            }
          ]
        }
      },
      "action_reason": "read_because_config_unknown"
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.aws_iam_policy.iam_policy[\"0\"]",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "managed",
      "type": "aws_iam_policy",
      "name": "iam_policy",
      "index": "0",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "delay_after_policy_creation_in_ms": null,
          "description": null,
          "name": "policy_0_dpf-bp-artifacts",
          "path": "/",
          "tags": null
        },
        "after_unknown": {
          "arn": true,
          "attachment_count": true,
          "id": true,
          "name_prefix": true,
          "policy": true,
          "policy_id": true,
          "tags_all": true
        },
        "before_sensitive": false,
        "after_sensitive": {
          "tags_all": {}
        },
        "after_identity": {
          "arn": null
        }
      }
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket.s3_bucket",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "managed",
      "type": "aws_s3_bucket",
      "name": "s3_bucket",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts",
          "force_destroy": true,
          "region": "eu-west-1",
          "tags": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3"
          },
          "tags_all": {
            "ApplicationID": "2102",
            "ApplicationName": "DATA PLATFORM FOUNDATION",
            "BuildingBlockName": "s3",
            "BuildingBlockVersion": "1.1.0",
            "Env": "sd",
            "Name": "s3"
          },
          "timeouts": null
        },
        "after_unknown": {
          "acceleration_status": true,
          "acl": true,
          "arn": true,
          "bucket_domain_name": true,
          "bucket_prefix": true,
          "bucket_region": true,
          "bucket_regional_domain_name": true,
          "cors_rule": true,
          "grant": true,
          "hosted_zone_id": true,
          "id": true,
          "lifecycle_rule": true,
          "logging": true,
          "object_lock_configuration": true,
          "object_lock_enabled": true,
          "policy": true,
          "replication_configuration": true,
          "request_payer": true,
          "server_side_encryption_configuration": true,
          "tags": {},
          "tags_all": {},
          "versioning": true,
          "website": true,
          "website_domain": true,
          "website_endpoint": true
        },
        "before_sensitive": false,
        "after_sensitive": {
          "cors_rule": [],
          "grant": [],
          "lifecycle_rule": [],
          "logging": [],
          "object_lock_configuration": [],
          "replication_configuration": [],
          "server_side_encryption_configuration": [],
          "tags": {},
          "tags_all": {},
          "versioning": [],
          "website": []
        },
        "after_identity": {
          "account_id": null,
          "bucket": null,
          "region": null
        }
      }
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket_logging.example",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "managed",
      "type": "aws_s3_bucket_logging",
      "name": "example",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "expected_bucket_owner": null,
          "region": "eu-west-1",
          "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {
                  "partition_date_source": "EventTime"
                }
              ],
              "simple_prefix": []
            }
          ],
          "target_prefix": "log/"
        },
        "after_unknown": {
          "bucket": true,
          "id": true,
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {}
              ],
              "simple_prefix": []
            }
          ]
        },
        "before_sensitive": false,
        "after_sensitive": {
          "target_grant": [],
          "target_object_key_format": [
            {
              "partitioned_prefix": [
                {}
              ],
              "simple_prefix": []
            }
          ]
        },
        "after_identity": {
          "account_id": null,
          "bucket": null,
          "region": null
        }
      }
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket_policy.bucket_policy",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "managed",
      "type": "aws_s3_bucket_policy",
      "name": "bucket_policy",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "region": "eu-west-1"
        },
        "after_unknown": {
          "bucket": true,
          "id": true,
          "policy": true
        },
        "before_sensitive": false,
        "after_sensitive": {},
        "after_identity": {
          "account_id": null,
          "bucket": null,
          "region": null
        }
      }
    },
    {
      "address": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket_public_access_block.public_access_block",
      "module_address": "module.blueprint.module.s3_bucket_artifacts",
      "mode": "managed",
      "type": "aws_s3_bucket_public_access_block",
      "name": "public_access_block",
      "provider_name": "registry.terraform.io/hashicorp/aws",
      "change": {
        "actions": [
          "create"
        ],
        "before": null,
        "after": {
          "block_public_acls": true,
          "block_public_policy": true,
          "ignore_public_acls": true,
          "region": "eu-west-1",
          "restrict_public_buckets": true,
          "skip_destroy": null
        },
        "after_unknown": {
          "bucket": true,
          "id": true
        },
        "before_sensitive": false,
        "after_sensitive": {},
        "after_identity": {
          "account_id": null,
          "bucket": null,
          "region": null
        }
      }
    }
  ],
  "prior_state": {
    "format_version": "1.0",
    "terraform_version": "1.13.5",
    "values": {
      "root_module": {
        "resources": [
          {
            "address": "data.aws_caller_identity.current",
            "mode": "data",
            "type": "aws_caller_identity",
            "name": "current",
            "provider_name": "registry.terraform.io/hashicorp/aws",
            "schema_version": 0,
            "values": {
              "account_id": "899076912694",
              "arn": "arn:aws:iam::899076912694:user/eniaws-sa-ictd-2102_pscoped_01",
              "id": "899076912694",
              "user_id": "AIDA5CVJI6Y3ARMQZ2JO3"
            },
            "sensitive_values": {}
          },
          {
            "address": "data.aws_region.current",
            "mode": "data",
            "type": "aws_region",
            "name": "current",
            "provider_name": "registry.terraform.io/hashicorp/aws",
            "schema_version": 0,
            "values": {
              "description": "Europe (Ireland)",
              "endpoint": "ec2.eu-west-1.amazonaws.com",
              "id": "eu-west-1",
              "name": "eu-west-1",
              "region": "eu-west-1"
            },
            "sensitive_values": {}
          }
        ],
        "child_modules": [
          {
            "resources": [
              {
                "address": "module.bb_blueprint.aws_cloudwatch_log_group.sf_logs",
                "mode": "managed",
                "type": "aws_cloudwatch_log_group",
                "name": "sf_logs",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "arn": "arn:aws:logs:eu-west-1:899076912694:log-group:eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test",
                  "deletion_protection_enabled": false,
                  "id": "eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test",
                  "kms_key_id": "arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
                  "log_group_class": "STANDARD",
                  "name": "eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test",
                  "name_prefix": "",
                  "region": "eu-west-1",
                  "retention_in_days": 365,
                  "skip_destroy": false,
                  "tags": {},
                  "tags_all": {}
                },
                "sensitive_values": {
                  "tags": {},
                  "tags_all": {}
                },
                "depends_on": [
                  "module.bb_blueprint.aws_iam_role.step_function_role",
                  "module.bb_blueprint.aws_kms_key.logs",
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current"
                ],
                "identity_schema_version": 0,
                "identity": {
                  "account_id": "899076912694",
                  "name": "eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test",
                  "region": "eu-west-1"
                }
              },
              {
                "address": "module.bb_blueprint.aws_cloudwatch_log_resource_policy.allow_sfn",
                "mode": "managed",
                "type": "aws_cloudwatch_log_resource_policy",
                "name": "allow_sfn",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "id": "AllowStepFunctionsToWriteSFLogs",
                  "policy_document": "{\"Statement\":[{\"Action\":[\"logs:CreateLogStream\",\"logs:PutLogEvents\",\"logs:DescribeLogStreams\"],\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"states.amazonaws.com\"},\"Resource\":\"arn:aws:logs:eu-west-1:899076912694:log-group:eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test:*\",\"Sid\":\"AllowSFN\"}],\"Version\":\"2012-10-17\"}",
                  "policy_name": "AllowStepFunctionsToWriteSFLogs",
                  "region": "eu-west-1"
                },
                "sensitive_values": {},
                "depends_on": [
                  "module.bb_blueprint.aws_cloudwatch_log_group.sf_logs",
                  "module.bb_blueprint.aws_iam_role.step_function_role",
                  "module.bb_blueprint.aws_kms_key.logs",
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current"
                ]
              },
              {
                "address": "module.bb_blueprint.aws_glue_catalog_table.databases[\"raw_db.logs.ExtractionErrors\"]",
                "mode": "managed",
                "type": "aws_glue_catalog_table",
                "name": "databases",
                "index": "raw_db.logs.ExtractionErrors",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "arn": "arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/extractionerrors",
                  "catalog_id": "899076912694",
                  "database_name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
                  "description": "",
                  "id": "899076912694:eniaws-glue-cat-euwe1-ictd-899076912694-raw:extractionerrors",
                  "name": "extractionerrors",
                  "open_table_format_input": [],
                  "owner": "",
                  "parameters": {
                    "format-version": "2"
                  },
                  "partition_index": [],
                  "partition_keys": [],
                  "region": "eu-west-1",
                  "retention": 0,
                  "storage_descriptor": [
                    {
                      "additional_locations": [],
                      "bucket_columns": [],
                      "columns": [
                        {
                          "comment": "",
                          "name": "entityname",
                          "parameters": {},
                          "type": "string"
                        },
                        {
                          "comment": "",
                          "name": "inputrowscount",
                          "parameters": {},
                          "type": "int"
                        },
                        {
                          "comment": "",
                          "name": "errorrowscount",
                          "parameters": {},
                          "type": "int"
                        },
                        {
                          "comment": "",
                          "name": "slicedate",
                          "parameters": {},
                          "type": "timestamp"
                        },
                        {
                          "comment": "",
                          "name": "runid",
                          "parameters": {},
                          "type": "string"
                        },
                        {
                          "comment": "",
                          "name": "isfullloading",
                          "parameters": {},
                          "type": "string"
                        }
                      ],
                      "compressed": false,
                      "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
                      "location": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/logs/ExtractionErrors/",
                      "number_of_buckets": 0,
                      "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
                      "parameters": {},
                      "schema_reference": [],
                      "ser_de_info": [
                        {
                          "name": "",
                          "parameters": {
                            "serialization.format": "1"
                          },
                          "serialization_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe"
                        }
                      ],
                      "skewed_info": [],
                      "sort_columns": [],
                      "stored_as_sub_directories": false
                    }
                  ],
                  "table_type": "ICEBERG",
                  "target_table": [],
                  "view_expanded_text": "",
                  "view_original_text": ""
                },
                "sensitive_values": {
                  "open_table_format_input": [],
                  "parameters": {},
                  "partition_index": [],
                  "partition_keys": [],
                  "storage_descriptor": [
                    {
                      "additional_locations": [],
                      "bucket_columns": [],
                      "columns": [
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        }
                      ],
                      "parameters": {},
                      "schema_reference": [],
                      "ser_de_info": [
                        {
                          "parameters": {}
                        }
                      ],
                      "skewed_info": [],
                      "sort_columns": []
                    }
                  ],
                  "target_table": []
                },
                "depends_on": [
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current",
                  "module.bb_blueprint.module.glue_catalog_database.aws_glue_catalog_database.catalog",
                  "module.bb_blueprint.module.glue_catalog_database.aws_iam_policy.iam_policy",
                  "module.bb_blueprint.module.glue_catalog_database.data.aws_caller_identity.current",
                  "module.bb_blueprint.module.glue_catalog_database.data.aws_iam_policy_document.custom_iam_policy_document",
                  "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket"
                ]
              },
              {
                "address": "module.bb_blueprint.aws_glue_catalog_table.databases[\"raw_db.logs.ExtractionErrorsDetail\"]",
                "mode": "managed",
                "type": "aws_glue_catalog_table",
                "name": "databases",
                "index": "raw_db.logs.ExtractionErrorsDetail",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "arn": "arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/extractionerrorsdetail",
                  "catalog_id": "899076912694",
                  "database_name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
                  "description": "",
                  "id": "899076912694:eniaws-glue-cat-euwe1-ictd-899076912694-raw:extractionerrorsdetail",
                  "name": "extractionerrorsdetail",
                  "open_table_format_input": [],
                  "owner": "",
                  "parameters": {
                    "format-version": "2"
                  },
                  "partition_index": [],
                  "partition_keys": [],
                  "region": "eu-west-1",
                  "retention": 0,
                  "storage_descriptor": [
                    {
                      "additional_locations": [],
                      "bucket_columns": [],
                      "columns": [
                        {
                          "comment": "",
                          "name": "entityname",
                          "parameters": {},
                          "type": "string"
                        },
                        {
                          "comment": "",
                          "name": "pk",
                          "parameters": {},
                          "type": "string"
                        },
                        {
                          "comment": "",
                          "name": "exceptions",
                          "parameters": {},
                          "type": "string"
                        },
                        {
                          "comment": "",
                          "name": "loadingslicedate",
                          "parameters": {},
                          "type": "string"
                        },
                        {
                          "comment": "",
                          "name": "auditinputfile",
                          "parameters": {},
                          "type": "string"
                        },
                        {
                          "comment": "",
                          "name": "auditfilecreationdatetime",
                          "parameters": {},
                          "type": "timestamp"
                        },
                        {
                          "comment": "",
                          "name": "auditcurrentdatetime",
                          "parameters": {},
                          "type": "timestamp"
                        },
                        {
                          "comment": "",
                          "name": "auditslicedate",
                          "parameters": {},
                          "type": "string"
                        },
                        {
                          "comment": "",
                          "name": "auditrunid",
                          "parameters": {},
                          "type": "string"
                        },
                        {
                          "comment": "",
                          "name": "auditisfullloading",
                          "parameters": {},
                          "type": "string"
                        }
                      ],
                      "compressed": false,
                      "input_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetInputFormat",
                      "location": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/logs/ExtractionErrorsDetail/",
                      "number_of_buckets": 0,
                      "output_format": "org.apache.hadoop.hive.ql.io.parquet.MapredParquetOutputFormat",
                      "parameters": {},
                      "schema_reference": [],
                      "ser_de_info": [
                        {
                          "name": "",
                          "parameters": {
                            "serialization.format": "1"
                          },
                          "serialization_library": "org.apache.hadoop.hive.ql.io.parquet.serde.ParquetHiveSerDe"
                        }
                      ],
                      "skewed_info": [],
                      "sort_columns": [],
                      "stored_as_sub_directories": false
                    }
                  ],
                  "table_type": "ICEBERG",
                  "target_table": [],
                  "view_expanded_text": "",
                  "view_original_text": ""
                },
                "sensitive_values": {
                  "open_table_format_input": [],
                  "parameters": {},
                  "partition_index": [],
                  "partition_keys": [],
                  "storage_descriptor": [
                    {
                      "additional_locations": [],
                      "bucket_columns": [],
                      "columns": [
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        },
                        {
                          "parameters": {}
                        }
                      ],
                      "parameters": {},
                      "schema_reference": [],
                      "ser_de_info": [
                        {
                          "parameters": {}
                        }
                      ],
                      "skewed_info": [],
                      "sort_columns": []
                    }
                  ],
                  "target_table": []
                },
                "depends_on": [
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current",
                  "module.bb_blueprint.module.glue_catalog_database.aws_glue_catalog_database.catalog",
                  "module.bb_blueprint.module.glue_catalog_database.aws_iam_policy.iam_policy",
                  "module.bb_blueprint.module.glue_catalog_database.data.aws_caller_identity.current",
                  "module.bb_blueprint.module.glue_catalog_database.data.aws_iam_policy_document.custom_iam_policy_document",
                  "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket"
                ]
              },
              {
                "address": "module.bb_blueprint.aws_iam_role.step_function_role[0]",
                "mode": "managed",
                "type": "aws_iam_role",
                "name": "step_function_role",
                "index": 0,
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "arn": "arn:aws:iam::899076912694:role/eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp",
                  "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"states.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
                  "create_date": "2026-02-13T15:23:45Z",
                  "description": "",
                  "force_detach_policies": false,
                  "id": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp",
                  "inline_policy": [
                    {
                      "name": "eniaws-sfn-role-euwe1-ictd-899076912694-dpf-bp",
                      "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"sns:Publish\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp\"}]}"
                    },
                    {
                      "name": "step-function-policy",
                      "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"lambda:InvokeFunction\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"},{\"Action\":[\"logs:CreateLogDelivery\",\"logs:GetLogDelivery\",\"logs:UpdateLogDelivery\",\"logs:DeleteLogDelivery\",\"logs:ListLogDeliveries\",\"logs:PutResourcePolicy\",\"logs:DescribeResourcePolicies\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:PutLogEvents\",\"logs:DescribeLogStreams\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test:*\"]},{\"Action\":[\"kms:Decrypt\",\"kms:Encrypt\",\"kms:GenerateDataKey\",\"kms:DescribeKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343\"]}]}"
                    }
                  ],
                  "managed_policy_arns": [],
                  "max_session_duration": 3600,
                  "name": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp",
                  "name_prefix": "",
                  "path": "/",
                  "permissions_boundary": "",
                  "tags": {},
                  "tags_all": {},
                  "unique_id": "AROA5CVJI6Y3GYQS2BVSA"
                },
                "sensitive_values": {
                  "inline_policy": [
                    {},
                    {}
                  ],
                  "managed_policy_arns": [],
                  "tags": {},
                  "tags_all": {}
                },
                "depends_on": [
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current"
                ],
                "identity_schema_version": 0,
                "identity": {
                  "account_id": "899076912694",
                  "name": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
                }
              },
              {
                "address": "module.bb_blueprint.aws_iam_role_policy.sfn_publish_sns[0]",
                "mode": "managed",
                "type": "aws_iam_role_policy",
                "name": "sfn_publish_sns",
                "index": 0,
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "id": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp:eniaws-sfn-role-euwe1-ictd-899076912694-dpf-bp",
                  "name": "eniaws-sfn-role-euwe1-ictd-899076912694-dpf-bp",
                  "name_prefix": "",
                  "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"sns:Publish\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp\"}]}",
                  "role": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
                },
                "sensitive_values": {},
                "depends_on": [
                  "module.bb_blueprint.aws_iam_role.step_function_role",
                  "module.bb_blueprint.aws_sns_topic.error_notification",
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current"
                ],
                "identity_schema_version": 0,
                "identity": {
                  "account_id": "899076912694",
                  "name": "eniaws-sfn-role-euwe1-ictd-899076912694-dpf-bp",
                  "role": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
                }
              },
              {
                "address": "module.bb_blueprint.aws_iam_role_policy.step_function_policy[0]",
                "mode": "managed",
                "type": "aws_iam_role_policy",
                "name": "step_function_policy",
                "index": 0,
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "id": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp:step-function-policy",
                  "name": "step-function-policy",
                  "name_prefix": "",
                  "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"lambda:InvokeFunction\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"},{\"Action\":[\"logs:CreateLogDelivery\",\"logs:GetLogDelivery\",\"logs:UpdateLogDelivery\",\"logs:DeleteLogDelivery\",\"logs:ListLogDeliveries\",\"logs:PutResourcePolicy\",\"logs:DescribeResourcePolicies\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:PutLogEvents\",\"logs:DescribeLogStreams\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:eniaws-logs-sf-euwe1-ictd-899076912694-dpf-bp-bb-step-function-alfa-test:*\"]},{\"Action\":[\"kms:Decrypt\",\"kms:Encrypt\",\"kms:GenerateDataKey\",\"kms:DescribeKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343\"]}]}",
                  "role": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
                },
                "sensitive_values": {},
                "depends_on": [
                  "module.bb_blueprint.aws_cloudwatch_log_group.sf_logs",
                  "module.bb_blueprint.aws_iam_role.step_function_role",
                  "module.bb_blueprint.aws_kms_key.logs",
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current",
                  "module.bb_blueprint.module.lambda_trigger.aws_iam_role.role",
                  "module.bb_blueprint.module.lambda_trigger.aws_lambda_function.func",
                  "module.bb_blueprint.module.lambda_trigger.aws_security_group.lambdansg",
                  "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.assume_role"
                ],
                "identity_schema_version": 0,
                "identity": {
                  "account_id": "899076912694",
                  "name": "step-function-policy",
                  "role": "eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp"
                }
              },
              {
                "address": "module.bb_blueprint.aws_kms_alias.logs",
                "mode": "managed",
                "type": "aws_kms_alias",
                "name": "logs",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "arn": "arn:aws:kms:eu-west-1:899076912694:alias/dp1453",
                  "id": "alias/dp1453",
                  "name": "alias/dp1453",
                  "name_prefix": "",
                  "region": "eu-west-1",
                  "target_key_arn": "arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
                  "target_key_id": "3c1b5c53-3d2d-4fd9-9889-93ba148e6343"
                },
                "sensitive_values": {},
                "depends_on": [
                  "module.bb_blueprint.aws_iam_role.step_function_role",
                  "module.bb_blueprint.aws_kms_key.logs",
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current"
                ],
                "identity_schema_version": 0,
                "identity": {
                  "account_id": "899076912694",
                  "name": "alias/dp1453",
                  "region": "eu-west-1"
                }
              },
              {
                "address": "module.bb_blueprint.aws_kms_key.logs",
                "mode": "managed",
                "type": "aws_kms_key",
                "name": "logs",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "arn": "arn:aws:kms:eu-west-1:899076912694:key/3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
                  "bypass_policy_lockout_safety_check": false,
                  "custom_key_store_id": "",
                  "customer_master_key_spec": "SYMMETRIC_DEFAULT",
                  "deletion_window_in_days": 7,
                  "description": "CMK for CloudWatch Logs encryption",
                  "enable_key_rotation": true,
                  "id": "3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
                  "is_enabled": true,
                  "key_id": "3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
                  "key_usage": "ENCRYPT_DECRYPT",
                  "multi_region": false,
                  "policy": "{\"Statement\":[{\"Action\":\"kms:*\",\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:root\"},\"Resource\":\"*\",\"Sid\":\"EnableRootPermissions\"},{\"Action\":[\"kms:Encrypt\",\"kms:Decrypt\",\"kms:ReEncrypt*\",\"kms:GenerateDataKey*\",\"kms:DescribeKey\"],\"Condition\":{\"ArnLike\":{\"kms:EncryptionContext:aws:logs:arn\":\"arn:aws:logs:eu-west-1:899076912694:log-group:*\"}},\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"logs.eu-west-1.amazonaws.com\"},\"Resource\":\"*\",\"Sid\":\"AllowCloudWatchLogsUseOfKey\"},{\"Action\":[\"kms:Encrypt\",\"kms:Decrypt\",\"kms:ReEncrypt*\",\"kms:GenerateDataKey*\",\"kms:DescribeKey\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp\"},\"Resource\":\"*\",\"Sid\":\"AllowStepFunctionUseOfKey\"},{\"Action\":[\"kms:CreateGrant\",\"kms:ListGrants\",\"kms:RevokeGrant\"],\"Condition\":{\"Bool\":{\"kms:GrantIsForAWSResource\":\"true\"}},\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"logs.eu-west-1.amazonaws.com\"},\"Resource\":\"*\",\"Sid\":\"AllowCloudWatchLogsGrants\"},{\"Action\":[\"kms:Encrypt\",\"kms:Decrypt\",\"kms:ReEncrypt*\",\"kms:GenerateDataKey*\",\"kms:DescribeKey\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/eniaws-step-function-role-euwe1-ictd-899076912694-dpf-bp\"},\"Resource\":\"*\",\"Sid\":\"AllowStepFunctionUseOfKey\"}],\"Version\":\"2012-10-17\"}",
                  "region": "eu-west-1",
                  "rotation_period_in_days": 365,
                  "tags": {},
                  "tags_all": {},
                  "timeouts": null,
                  "xks_key_id": ""
                },
                "sensitive_values": {
                  "tags": {},
                  "tags_all": {}
                },
                "depends_on": [
                  "module.bb_blueprint.aws_iam_role.step_function_role",
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current"
                ],
                "identity_schema_version": 0,
                "identity": {
                  "account_id": "899076912694",
                  "id": "3c1b5c53-3d2d-4fd9-9889-93ba148e6343",
                  "region": "eu-west-1"
                }
              },
              {
                "address": "module.bb_blueprint.aws_s3_bucket_notification.notify_lambda",
                "mode": "managed",
                "type": "aws_s3_bucket_notification",
                "name": "notify_lambda",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                  "eventbridge": false,
                  "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                  "lambda_function": [
                    {
                      "events": [
                        "s3:ObjectCreated:*"
                      ],
                      "filter_prefix": "",
                      "filter_suffix": "",
                      "id": "tf-s3-lambda-20260212093842339000000001",
                      "lambda_function_arn": "arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test"
                    }
                  ],
                  "queue": [],
                  "region": "eu-west-1",
                  "topic": []
                },
                "sensitive_values": {
                  "lambda_function": [
                    {
                      "events": [
                        false
                      ]
                    }
                  ],
                  "queue": [],
                  "topic": []
                },
                "depends_on": [
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current",
                  "module.bb_blueprint.module.lambda_trigger.aws_iam_role.role",
                  "module.bb_blueprint.module.lambda_trigger.aws_lambda_function.func",
                  "module.bb_blueprint.module.lambda_trigger.aws_security_group.lambdansg",
                  "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.assume_role",
                  "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket"
                ],
                "identity_schema_version": 0,
                "identity": {
                  "account_id": "899076912694",
                  "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                  "region": "eu-west-1"
                }
              },
              {
                "address": "module.bb_blueprint.aws_sns_topic.error_notification",
                "mode": "managed",
                "type": "aws_sns_topic",
                "name": "error_notification",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "application_failure_feedback_role_arn": "",
                  "application_success_feedback_role_arn": "",
                  "application_success_feedback_sample_rate": 0,
                  "archive_policy": "",
                  "arn": "arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp",
                  "beginning_archive_time": "",
                  "content_based_deduplication": false,
                  "delivery_policy": "",
                  "display_name": "",
                  "fifo_throughput_scope": "",
                  "fifo_topic": false,
                  "firehose_failure_feedback_role_arn": "",
                  "firehose_success_feedback_role_arn": "",
                  "firehose_success_feedback_sample_rate": 0,
                  "http_failure_feedback_role_arn": "",
                  "http_success_feedback_role_arn": "",
                  "http_success_feedback_sample_rate": 0,
                  "id": "arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp",
                  "kms_master_key_id": "alias/aws/sns",
                  "lambda_failure_feedback_role_arn": "",
                  "lambda_success_feedback_role_arn": "",
                  "lambda_success_feedback_sample_rate": 0,
                  "name": "eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp",
                  "name_prefix": "",
                  "owner": "899076912694",
                  "policy": "{\"Id\":\"__default_policy_ID\",\"Statement\":[{\"Action\":[\"SNS:GetTopicAttributes\",\"SNS:SetTopicAttributes\",\"SNS:AddPermission\",\"SNS:RemovePermission\",\"SNS:DeleteTopic\",\"SNS:Subscribe\",\"SNS:ListSubscriptionsByTopic\",\"SNS:Publish\"],\"Condition\":{\"StringEquals\":{\"AWS:SourceOwner\":\"899076912694\"}},\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"*\"},\"Resource\":\"arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp\",\"Sid\":\"__default_statement_ID\"}],\"Version\":\"2008-10-17\"}",
                  "region": "eu-west-1",
                  "signature_version": 0,
                  "sqs_failure_feedback_role_arn": "",
                  "sqs_success_feedback_role_arn": "",
                  "sqs_success_feedback_sample_rate": 0,
                  "tags": {},
                  "tags_all": {},
                  "tracing_config": ""
                },
                "sensitive_values": {
                  "tags": {},
                  "tags_all": {}
                },
                "depends_on": [
                  "module.bb_blueprint.data.aws_caller_identity.current",
                  "module.bb_blueprint.data.aws_region.current"
                ],
                "identity_schema_version": 0,
                "identity": {
                  "arn": "arn:aws:sns:eu-west-1:899076912694:eniaws-sns-topic-euwe1-ictd-899076912694-dpf-bp"
                }
              }
            ],
            "address": "module.bb_blueprint",
            "child_modules": [
              {
                "resources": [
                  {
                    "address": "module.bb_blueprint.module.glue_catalog_database[\"raw_db\"].aws_glue_catalog_database.catalog",
                    "mode": "managed",
                    "type": "aws_glue_catalog_database",
                    "name": "catalog",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw",
                      "catalog_id": "899076912694",
                      "create_table_default_permission": [
                        {
                          "permissions": [
                            "ALL"
                          ],
                          "principal": [
                            {
                              "data_lake_principal_identifier": "IAM_ALLOWED_PRINCIPALS"
                            }
                          ]
                        }
                      ],
                      "description": "Glue database per i dati raw",
                      "federated_database": [],
                      "id": "899076912694:eniaws-glue-cat-euwe1-ictd-899076912694-raw",
                      "location_uri": "",
                      "name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
                      "parameters": {},
                      "region": "eu-west-1",
                      "tags": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "Env": "sd"
                      },
                      "tags_all": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "Env": "sd"
                      },
                      "target_database": []
                    },
                    "sensitive_values": {
                      "create_table_default_permission": [
                        {
                          "permissions": [
                            false
                          ],
                          "principal": [
                            {}
                          ]
                        }
                      ],
                      "federated_database": [],
                      "parameters": {},
                      "tags": {},
                      "tags_all": {},
                      "target_database": []
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current"
                    ]
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_catalog_database[\"raw_db\"].aws_iam_policy.iam_policy[\"0\"]",
                    "mode": "managed",
                    "type": "aws_iam_policy",
                    "name": "iam_policy",
                    "index": "0",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_glue_db_0_raw",
                      "attachment_count": 0,
                      "delay_after_policy_creation_in_ms": null,
                      "description": "",
                      "id": "arn:aws:iam::899076912694:policy/policy_glue_db_0_raw",
                      "name": "policy_glue_db_0_raw",
                      "name_prefix": "",
                      "path": "/",
                      "policy": "{\"Statement\":[{\"Action\":[\"glue:GetTables\",\"glue:GetDatabase\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/raw_db/*\",\"arn:aws:glue:eu-west-1:899076912694:database/raw_db\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueDatabaseRead\"}],\"Version\":\"2012-10-17\"}",
                      "policy_id": "ANPA5CVJI6Y3OPADRRZ46",
                      "tags": {},
                      "tags_all": {}
                    },
                    "sensitive_values": {
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_catalog_database.data.aws_iam_policy_document.custom_iam_policy_document"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_glue_db_0_raw"
                    }
                  }
                ],
                "address": "module.bb_blueprint.module.glue_catalog_database[\"raw_db\"]"
              },
              {
                "resources": [
                  {
                    "address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"].aws_glue_crawler.crawler",
                    "mode": "managed",
                    "type": "aws_glue_crawler",
                    "name": "crawler",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:glue:eu-west-1:899076912694:crawler/eniaws-glue-crw-euwe1-ictd-899076912694-dpf-bp",
                      "catalog_target": [],
                      "classifiers": [],
                      "configuration": "",
                      "database_name": "eniaws-glue-cat-euwe1-ictd-899076912694-raw",
                      "delta_target": [],
                      "description": "",
                      "dynamodb_target": [],
                      "hudi_target": [],
                      "iceberg_target": [],
                      "id": "eniaws-glue-crw-euwe1-ictd-899076912694-dpf-bp",
                      "jdbc_target": [],
                      "lake_formation_configuration": [
                        {
                          "account_id": "",
                          "use_lake_formation_credentials": false
                        }
                      ],
                      "lineage_configuration": [
                        {
                          "crawler_lineage_settings": "ENABLE"
                        }
                      ],
                      "mongodb_target": [],
                      "name": "eniaws-glue-crw-euwe1-ictd-899076912694-dpf-bp",
                      "recrawl_policy": [
                        {
                          "recrawl_behavior": "CRAWL_EVERYTHING"
                        }
                      ],
                      "region": "eu-west-1",
                      "role": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp",
                      "s3_target": [
                        {
                          "connection_name": "",
                          "dlq_event_queue_arn": "",
                          "event_queue_arn": "",
                          "exclusions": [],
                          "path": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/raw/",
                          "sample_size": 0
                        }
                      ],
                      "schedule": "cron(0 12 * * ? *)",
                      "schema_change_policy": [
                        {
                          "delete_behavior": "LOG",
                          "update_behavior": "UPDATE_IN_DATABASE"
                        }
                      ],
                      "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l1-l2",
                      "table_prefix": "sd_",
                      "tags": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "Env": "sd",
                        "Name": "glue_crawler"
                      },
                      "tags_all": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "Env": "sd",
                        "Name": "glue_crawler"
                      }
                    },
                    "sensitive_values": {
                      "catalog_target": [],
                      "classifiers": [],
                      "delta_target": [],
                      "dynamodb_target": [],
                      "hudi_target": [],
                      "iceberg_target": [],
                      "jdbc_target": [],
                      "lake_formation_configuration": [
                        {}
                      ],
                      "lineage_configuration": [
                        {}
                      ],
                      "mongodb_target": [],
                      "recrawl_policy": [
                        {}
                      ],
                      "s3_target": [
                        {
                          "exclusions": []
                        }
                      ],
                      "schema_change_policy": [
                        {}
                      ],
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_catalog_database.aws_glue_catalog_database.catalog",
                      "module.bb_blueprint.module.glue_catalog_database.aws_iam_policy.iam_policy",
                      "module.bb_blueprint.module.glue_catalog_database.data.aws_caller_identity.current",
                      "module.bb_blueprint.module.glue_catalog_database.data.aws_iam_policy_document.custom_iam_policy_document",
                      "module.bb_blueprint.module.glue_crawler.aws_iam_role.role",
                      "module.bb_blueprint.module.glue_crawler.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.glue_job_2.aws_glue_security_configuration.this",
                      "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket.s3_bucket"
                    ]
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"].aws_iam_role.role",
                    "mode": "managed",
                    "type": "aws_iam_role",
                    "name": "role",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:iam::899076912694:role/eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp",
                      "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
                      "create_date": "2026-02-12T09:35:21Z",
                      "description": "",
                      "force_detach_policies": false,
                      "id": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp",
                      "inline_policy": [
                        {
                          "name": "glue_crawler_permissions",
                          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":\"s3:ListBucket\",\"Condition\":{\"StringLike\":{\"s3:prefix\":[\"raw//*\",\"raw/\"]}},\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"Sid\":\"S3ListBucket\"},{\"Action\":\"s3:GetObject\",\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/raw//*\",\"Sid\":\"S3ReadObjects\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:GetTables\",\"glue:GetTable\",\"glue:GetDatabases\",\"glue:GetDatabase\",\"glue:CreateTable\",\"glue:CreatePartition\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueCatalogDbTableAccess\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"],\"Sid\":\"GlueCrawlerLogs\"},{\"Action\":[\"glue:GetSecurityConfigurations\",\"glue:GetSecurityConfiguration\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"GlueSecurityConfigurationAccess\"},{\"Action\":\"glue:GetSecurityConfiguration\",\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"AllowGetSecurityConfiguration\"}]}"
                        }
                      ],
                      "managed_policy_arns": [],
                      "max_session_duration": 3600,
                      "name": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp",
                      "name_prefix": "",
                      "path": "/",
                      "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
                      "tags": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "Env": "sd",
                        "Name": "glue_crawler"
                      },
                      "tags_all": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "Env": "sd",
                        "Name": "glue_crawler"
                      },
                      "unique_id": "AROA5CVJI6Y3NYCDVCJQX"
                    },
                    "sensitive_values": {
                      "inline_policy": [
                        {}
                      ],
                      "managed_policy_arns": [],
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_catalog_database.aws_glue_catalog_database.catalog",
                      "module.bb_blueprint.module.glue_catalog_database.aws_iam_policy.iam_policy",
                      "module.bb_blueprint.module.glue_catalog_database.data.aws_caller_identity.current",
                      "module.bb_blueprint.module.glue_catalog_database.data.aws_iam_policy_document.custom_iam_policy_document",
                      "module.bb_blueprint.module.glue_crawler.data.aws_iam_policy_document.assume_role"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "name": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"].aws_iam_role_policy.glue_crawler_permissions",
                    "mode": "managed",
                    "type": "aws_iam_role_policy",
                    "name": "glue_crawler_permissions",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp:glue_crawler_permissions",
                      "name": "glue_crawler_permissions",
                      "name_prefix": "",
                      "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":\"s3:ListBucket\",\"Condition\":{\"StringLike\":{\"s3:prefix\":[\"raw//*\",\"raw/\"]}},\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"Sid\":\"S3ListBucket\"},{\"Action\":\"s3:GetObject\",\"Effect\":\"Allow\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/raw//*\",\"Sid\":\"S3ReadObjects\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:GetTables\",\"glue:GetTable\",\"glue:GetDatabases\",\"glue:GetDatabase\",\"glue:CreateTable\",\"glue:CreatePartition\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueCatalogDbTableAccess\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"],\"Sid\":\"GlueCrawlerLogs\"},{\"Action\":[\"glue:GetSecurityConfigurations\",\"glue:GetSecurityConfiguration\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"GlueSecurityConfigurationAccess\"},{\"Action\":\"glue:GetSecurityConfiguration\",\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"AllowGetSecurityConfiguration\"}]}",
                      "role": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp"
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_catalog_database.aws_glue_catalog_database.catalog",
                      "module.bb_blueprint.module.glue_catalog_database.aws_iam_policy.iam_policy",
                      "module.bb_blueprint.module.glue_catalog_database.data.aws_caller_identity.current",
                      "module.bb_blueprint.module.glue_catalog_database.data.aws_iam_policy_document.custom_iam_policy_document",
                      "module.bb_blueprint.module.glue_crawler.aws_iam_role.role",
                      "module.bb_blueprint.module.glue_crawler.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.glue_crawler.data.aws_iam_policy_document.combined",
                      "module.bb_blueprint.module.glue_crawler.data.aws_iam_policy_document.custom_iam_policy_document",
                      "module.bb_blueprint.module.glue_crawler.data.aws_iam_policy_document.glue_crawler_policy",
                      "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket.s3_bucket"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "name": "glue_crawler_permissions",
                      "role": "eniaws-glue-crawler-role-euwe1-ictd-899076912694-dpf-bp"
                    }
                  }
                ],
                "address": "module.bb_blueprint.module.glue_crawler[\"raw_db\"]"
              },
              {
                "resources": [
                  {
                    "address": "module.bb_blueprint.module.glue_job_1.aws_glue_connection.network",
                    "mode": "managed",
                    "type": "aws_glue_connection",
                    "name": "network",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
                      "athena_properties": {},
                      "catalog_id": "899076912694",
                      "connection_properties": {},
                      "connection_type": "NETWORK",
                      "description": "",
                      "id": "899076912694:eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
                      "match_criteria": [],
                      "name": "eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
                      "physical_connection_requirements": [
                        {
                          "availability_zone": "eu-west-1a",
                          "security_group_id_list": [
                            "sg-032c47f80254c35c7",
                            "sg-09096e91dd18fa7d4",
                            "sg-0aa6fd5972038141a",
                            "sg-0cb505f744b1c74eb"
                          ],
                          "subnet_id": "subnet-0a8409260cbaf999f"
                        }
                      ],
                      "region": "eu-west-1",
                      "tags": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "BuildingBlockName": "aws_glue",
                        "BuildingBlockVersion": "0.0.0",
                        "Env": "env",
                        "Name": "job1"
                      },
                      "tags_all": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "BuildingBlockName": "aws_glue",
                        "BuildingBlockVersion": "0.0.0",
                        "Env": "env",
                        "Name": "job1"
                      }
                    },
                    "sensitive_values": {
                      "athena_properties": true,
                      "connection_properties": true,
                      "match_criteria": [],
                      "physical_connection_requirements": [
                        {
                          "security_group_id_list": [
                            false,
                            false,
                            false,
                            false
                          ]
                        }
                      ],
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current"
                    ]
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_job_1.aws_glue_job.job",
                    "mode": "managed",
                    "type": "aws_glue_job",
                    "name": "job",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:glue:eu-west-1:899076912694:job/eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
                      "command": [
                        {
                          "name": "glueetl",
                          "python_version": "3",
                          "runtime": "",
                          "script_location": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/glue_jobs/src/extraction.py"
                        }
                      ],
                      "connections": [
                        "eniaws-glue-euwe1-ictd-899076912694-job-l0-l1"
                      ],
                      "default_arguments": {
                        "--continuous-log-logGroup": "/aws-glue/jobs",
                        "--enable-auto-scaling": "true",
                        "--enable-continuous-cloudwatch-log": "true",
                        "--enable-continuous-log-filter": "true",
                        "--enable-job-insights": "true",
                        "--enable-metrics": "",
                        "--enable-observability-metrics": "true",
                        "--input_path": "",
                        "--job-language": "python",
                        "--output_path": ""
                      },
                      "description": "Glue Job",
                      "execution_class": "STANDARD",
                      "execution_property": [
                        {
                          "max_concurrent_runs": 1
                        }
                      ],
                      "glue_version": "4.0",
                      "id": "eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
                      "job_mode": "SCRIPT",
                      "job_run_queuing_enabled": false,
                      "maintenance_window": "",
                      "max_capacity": 10,
                      "max_retries": 0,
                      "name": "eniaws-glue-euwe1-ictd-899076912694-job-l0-l1",
                      "non_overridable_arguments": {},
                      "notification_property": [],
                      "number_of_workers": 10,
                      "region": "eu-west-1",
                      "role_arn": "arn:aws:iam::899076912694:role/eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1",
                      "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l0-l1",
                      "source_control_details": [],
                      "tags": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "BuildingBlockName": "aws_glue",
                        "BuildingBlockVersion": "0.0.0",
                        "Env": "env",
                        "Name": "job1"
                      },
                      "tags_all": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "BuildingBlockName": "aws_glue",
                        "BuildingBlockVersion": "0.0.0",
                        "Env": "env",
                        "Name": "job1"
                      },
                      "timeout": 2880,
                      "worker_type": "G.1X"
                    },
                    "sensitive_values": {
                      "command": [
                        {}
                      ],
                      "connections": [
                        false
                      ],
                      "default_arguments": {},
                      "execution_property": [
                        {}
                      ],
                      "non_overridable_arguments": {},
                      "notification_property": [],
                      "source_control_details": [],
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_job_1.aws_glue_connection.network",
                      "module.bb_blueprint.module.glue_job_1.aws_glue_security_configuration.this",
                      "module.bb_blueprint.module.glue_job_1.aws_iam_role.role",
                      "module.bb_blueprint.module.glue_job_1.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket"
                    ]
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_job_1.aws_glue_security_configuration.this",
                    "mode": "managed",
                    "type": "aws_glue_security_configuration",
                    "name": "this",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "encryption_configuration": [
                        {
                          "cloudwatch_encryption": [
                            {
                              "cloudwatch_encryption_mode": "SSE-KMS",
                              "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/logs"
                            }
                          ],
                          "job_bookmarks_encryption": [
                            {
                              "job_bookmarks_encryption_mode": "CSE-KMS",
                              "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/glue"
                            }
                          ],
                          "s3_encryption": [
                            {
                              "kms_key_arn": "",
                              "s3_encryption_mode": "SSE-S3"
                            }
                          ]
                        }
                      ],
                      "id": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l0-l1",
                      "name": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l0-l1",
                      "region": "eu-west-1"
                    },
                    "sensitive_values": {
                      "encryption_configuration": [
                        {
                          "cloudwatch_encryption": [
                            {}
                          ],
                          "job_bookmarks_encryption": [
                            {}
                          ],
                          "s3_encryption": [
                            {}
                          ]
                        }
                      ]
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current"
                    ]
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_job_1.aws_iam_role.role",
                    "mode": "managed",
                    "type": "aws_iam_role",
                    "name": "role",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:iam::899076912694:role/eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1",
                      "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
                      "create_date": "2026-02-12T09:35:20Z",
                      "description": "",
                      "force_detach_policies": false,
                      "id": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1",
                      "inline_policy": [
                        {
                          "name": "glue_job_permissions",
                          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"s3:PutObject\",\"s3:ListBucket\",\"s3:GetObject\",\"s3:GetBucketLocation\",\"s3:DeleteObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"S3Access\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"LogsAccess\"},{\"Action\":\"cloudwatch:PutMetricData\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"CloudWatchMetrics\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:SearchTables\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"GlueAccess\"},{\"Action\":[\"ec2:GetConnectionStatus\",\"ec2:Describe*\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"EC2Describe\"},{\"Action\":[\"ec2:DetachNetworkInterface\",\"ec2:DeleteNetworkInterface\",\"ec2:CreateNetworkInterface\",\"ec2:AttachNetworkInterface\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7\",\"arn:aws:ec2:eu-west-1:899076912694:network-interface/*\"],\"Sid\":\"EC2Modify\"},{\"Action\":[\"glue:GetConnections\",\"glue:GetConnection\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l0-l1\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueConnectionRead\"},{\"Action\":[\"ec2:DescribeVpcs\",\"ec2:DescribeVpcEndpoints\",\"ec2:DescribeSubnets\",\"ec2:DescribeSecurityGroups\",\"ec2:DescribeRouteTables\",\"ec2:DescribeNetworkInterfaces\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"EC2DescribeForGlueNetwork\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"AllowRestrictedGlueActions\"},{\"Action\":[\"logs:DisassociateKmsKey\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*\",\"arn:aws:kms:eu-west-1:899076912694:alias/aws/glue\"],\"Sid\":\"AllowCloudWatchLogsAssociateKmsKey\"}]}"
                        }
                      ],
                      "managed_policy_arns": [],
                      "max_session_duration": 3600,
                      "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1",
                      "name_prefix": "",
                      "path": "/",
                      "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
                      "tags": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "Env": "env",
                        "Name": "job1"
                      },
                      "tags_all": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "Env": "env",
                        "Name": "job1"
                      },
                      "unique_id": "AROA5CVJI6Y3ANO43V6JZ"
                    },
                    "sensitive_values": {
                      "inline_policy": [
                        {}
                      ],
                      "managed_policy_arns": [],
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_job_1.data.aws_iam_policy_document.assume_role"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_job_1.aws_iam_role_policy.glue_job_permissions",
                    "mode": "managed",
                    "type": "aws_iam_role_policy",
                    "name": "glue_job_permissions",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1:glue_job_permissions",
                      "name": "glue_job_permissions",
                      "name_prefix": "",
                      "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"s3:PutObject\",\"s3:ListBucket\",\"s3:GetObject\",\"s3:GetBucketLocation\",\"s3:DeleteObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"S3Access\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"LogsAccess\"},{\"Action\":\"cloudwatch:PutMetricData\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"CloudWatchMetrics\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:SearchTables\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"GlueAccess\"},{\"Action\":[\"ec2:GetConnectionStatus\",\"ec2:Describe*\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"EC2Describe\"},{\"Action\":[\"ec2:DetachNetworkInterface\",\"ec2:DeleteNetworkInterface\",\"ec2:CreateNetworkInterface\",\"ec2:AttachNetworkInterface\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7\",\"arn:aws:ec2:eu-west-1:899076912694:network-interface/*\"],\"Sid\":\"EC2Modify\"},{\"Action\":[\"glue:GetConnections\",\"glue:GetConnection\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l0-l1\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueConnectionRead\"},{\"Action\":[\"ec2:DescribeVpcs\",\"ec2:DescribeVpcEndpoints\",\"ec2:DescribeSubnets\",\"ec2:DescribeSecurityGroups\",\"ec2:DescribeRouteTables\",\"ec2:DescribeNetworkInterfaces\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"EC2DescribeForGlueNetwork\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"AllowRestrictedGlueActions\"},{\"Action\":[\"logs:DisassociateKmsKey\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*\",\"arn:aws:kms:eu-west-1:899076912694:alias/aws/glue\"],\"Sid\":\"AllowCloudWatchLogsAssociateKmsKey\"}]}",
                      "role": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1"
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_job_1.aws_glue_connection.network",
                      "module.bb_blueprint.module.glue_job_1.aws_iam_role.role",
                      "module.bb_blueprint.module.glue_job_1.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.glue_job_1.data.aws_iam_policy_document.custom_iam_policy_document",
                      "module.bb_blueprint.module.glue_job_1.data.aws_iam_policy_document.glue_job_combined_policy",
                      "module.bb_blueprint.module.glue_job_1.data.aws_iam_policy_document.glue_job_policy",
                      "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket.s3_bucket"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "name": "glue_job_permissions",
                      "role": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l0-l1"
                    }
                  }
                ],
                "address": "module.bb_blueprint.module.glue_job_1"
              },
              {
                "resources": [
                  {
                    "address": "module.bb_blueprint.module.glue_job_2.aws_glue_connection.network",
                    "mode": "managed",
                    "type": "aws_glue_connection",
                    "name": "network",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
                      "athena_properties": {},
                      "catalog_id": "899076912694",
                      "connection_properties": {},
                      "connection_type": "NETWORK",
                      "description": "",
                      "id": "899076912694:eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
                      "match_criteria": [],
                      "name": "eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
                      "physical_connection_requirements": [
                        {
                          "availability_zone": "eu-west-1a",
                          "security_group_id_list": [
                            "sg-032c47f80254c35c7",
                            "sg-09096e91dd18fa7d4",
                            "sg-0aa6fd5972038141a",
                            "sg-0cb505f744b1c74eb"
                          ],
                          "subnet_id": "subnet-0a8409260cbaf999f"
                        }
                      ],
                      "region": "eu-west-1",
                      "tags": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "BuildingBlockName": "aws_glue",
                        "BuildingBlockVersion": "0.0.0",
                        "Env": "env",
                        "Name": "job2"
                      },
                      "tags_all": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "BuildingBlockName": "aws_glue",
                        "BuildingBlockVersion": "0.0.0",
                        "Env": "env",
                        "Name": "job2"
                      }
                    },
                    "sensitive_values": {
                      "athena_properties": true,
                      "connection_properties": true,
                      "match_criteria": [],
                      "physical_connection_requirements": [
                        {
                          "security_group_id_list": [
                            false,
                            false,
                            false,
                            false
                          ]
                        }
                      ],
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current"
                    ]
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_job_2.aws_glue_job.job",
                    "mode": "managed",
                    "type": "aws_glue_job",
                    "name": "job",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:glue:eu-west-1:899076912694:job/eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
                      "command": [
                        {
                          "name": "glueetl",
                          "python_version": "3",
                          "runtime": "",
                          "script_location": "s3://eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/glue_jobs/src/quality.py"
                        }
                      ],
                      "connections": [
                        "eniaws-glue-euwe1-ictd-899076912694-job-l1-l2"
                      ],
                      "default_arguments": {
                        "--continuous-log-logGroup": "/aws-glue/jobs",
                        "--enable-auto-scaling": "true",
                        "--enable-continuous-cloudwatch-log": "true",
                        "--enable-continuous-log-filter": "true",
                        "--enable-job-insights": "true",
                        "--enable-metrics": "",
                        "--enable-observability-metrics": "true",
                        "--input_path": "",
                        "--job-language": "python",
                        "--output_path": ""
                      },
                      "description": "Glue Job",
                      "execution_class": "STANDARD",
                      "execution_property": [
                        {
                          "max_concurrent_runs": 1
                        }
                      ],
                      "glue_version": "4.0",
                      "id": "eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
                      "job_mode": "SCRIPT",
                      "job_run_queuing_enabled": false,
                      "maintenance_window": "",
                      "max_capacity": 10,
                      "max_retries": 0,
                      "name": "eniaws-glue-euwe1-ictd-899076912694-job-l1-l2",
                      "non_overridable_arguments": {},
                      "notification_property": [],
                      "number_of_workers": 10,
                      "region": "eu-west-1",
                      "role_arn": "arn:aws:iam::899076912694:role/eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2",
                      "security_configuration": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l1-l2",
                      "source_control_details": [],
                      "tags": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "BuildingBlockName": "aws_glue",
                        "BuildingBlockVersion": "0.0.0",
                        "Env": "env",
                        "Name": "job2"
                      },
                      "tags_all": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "BuildingBlockName": "aws_glue",
                        "BuildingBlockVersion": "0.0.0",
                        "Env": "env",
                        "Name": "job2"
                      },
                      "timeout": 2880,
                      "worker_type": "G.1X"
                    },
                    "sensitive_values": {
                      "command": [
                        {}
                      ],
                      "connections": [
                        false
                      ],
                      "default_arguments": {},
                      "execution_property": [
                        {}
                      ],
                      "non_overridable_arguments": {},
                      "notification_property": [],
                      "source_control_details": [],
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_job_2.aws_glue_connection.network",
                      "module.bb_blueprint.module.glue_job_2.aws_glue_security_configuration.this",
                      "module.bb_blueprint.module.glue_job_2.aws_iam_role.role",
                      "module.bb_blueprint.module.glue_job_2.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket"
                    ]
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_job_2.aws_glue_security_configuration.this",
                    "mode": "managed",
                    "type": "aws_glue_security_configuration",
                    "name": "this",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "encryption_configuration": [
                        {
                          "cloudwatch_encryption": [
                            {
                              "cloudwatch_encryption_mode": "SSE-KMS",
                              "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/logs"
                            }
                          ],
                          "job_bookmarks_encryption": [
                            {
                              "job_bookmarks_encryption_mode": "CSE-KMS",
                              "kms_key_arn": "arn:aws:kms:eu-west-1:899076912694:alias/aws/glue"
                            }
                          ],
                          "s3_encryption": [
                            {
                              "kms_key_arn": "",
                              "s3_encryption_mode": "SSE-S3"
                            }
                          ]
                        }
                      ],
                      "id": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l1-l2",
                      "name": "eniaws-glue-sec-euwe1-ictd-899076912694-job-l1-l2",
                      "region": "eu-west-1"
                    },
                    "sensitive_values": {
                      "encryption_configuration": [
                        {
                          "cloudwatch_encryption": [
                            {}
                          ],
                          "job_bookmarks_encryption": [
                            {}
                          ],
                          "s3_encryption": [
                            {}
                          ]
                        }
                      ]
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current"
                    ]
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_job_2.aws_iam_role.role",
                    "mode": "managed",
                    "type": "aws_iam_role",
                    "name": "role",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:iam::899076912694:role/eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2",
                      "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
                      "create_date": "2026-02-12T09:35:19Z",
                      "description": "",
                      "force_detach_policies": false,
                      "id": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2",
                      "inline_policy": [
                        {
                          "name": "glue_job_permissions",
                          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"s3:PutObject\",\"s3:ListBucket\",\"s3:GetObject\",\"s3:GetBucketLocation\",\"s3:DeleteObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"S3Access\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"LogsAccess\"},{\"Action\":\"cloudwatch:PutMetricData\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"CloudWatchMetrics\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:SearchTables\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"GlueAccess\"},{\"Action\":[\"ec2:GetConnectionStatus\",\"ec2:Describe*\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"EC2Describe\"},{\"Action\":[\"ec2:DetachNetworkInterface\",\"ec2:DeleteNetworkInterface\",\"ec2:CreateNetworkInterface\",\"ec2:AttachNetworkInterface\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7\",\"arn:aws:ec2:eu-west-1:899076912694:network-interface/*\"],\"Sid\":\"EC2Modify\"},{\"Action\":[\"glue:GetConnections\",\"glue:GetConnection\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l1-l2\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueConnectionRead\"},{\"Action\":[\"ec2:DescribeVpcs\",\"ec2:DescribeVpcEndpoints\",\"ec2:DescribeSubnets\",\"ec2:DescribeSecurityGroups\",\"ec2:DescribeRouteTables\",\"ec2:DescribeNetworkInterfaces\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"EC2DescribeForGlueNetwork\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"AllowRestrictedGlueActions\"},{\"Action\":[\"logs:DisassociateKmsKey\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*\",\"arn:aws:kms:eu-west-1:899076912694:alias/aws/glue\"],\"Sid\":\"AllowCloudWatchLogsAssociateKmsKey\"}]}"
                        }
                      ],
                      "managed_policy_arns": [],
                      "max_session_duration": 3600,
                      "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2",
                      "name_prefix": "",
                      "path": "/",
                      "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
                      "tags": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "Env": "env",
                        "Name": "job2"
                      },
                      "tags_all": {
                        "ApplicationID": "id",
                        "ApplicationName": "test",
                        "Env": "env",
                        "Name": "job2"
                      },
                      "unique_id": "AROA5CVJI6Y3J3EVLFBB5"
                    },
                    "sensitive_values": {
                      "inline_policy": [
                        {}
                      ],
                      "managed_policy_arns": [],
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_job_2.data.aws_iam_policy_document.assume_role"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "name": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.glue_job_2.aws_iam_role_policy.glue_job_permissions",
                    "mode": "managed",
                    "type": "aws_iam_role_policy",
                    "name": "glue_job_permissions",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2:glue_job_permissions",
                      "name": "glue_job_permissions",
                      "name_prefix": "",
                      "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"s3:PutObject\",\"s3:ListBucket\",\"s3:GetObject\",\"s3:GetBucketLocation\",\"s3:DeleteObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"S3Access\"},{\"Action\":[\"logs:PutLogEvents\",\"logs:DescribeLogGroups\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"LogsAccess\"},{\"Action\":\"cloudwatch:PutMetricData\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"CloudWatchMetrics\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:SearchTables\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"GlueAccess\"},{\"Action\":[\"ec2:GetConnectionStatus\",\"ec2:Describe*\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:*:*:log-group:/aws-glue/*:*\",\"arn:aws:logs:*:*:log-group:/aws-glue/*\"],\"Sid\":\"EC2Describe\"},{\"Action\":[\"ec2:DetachNetworkInterface\",\"ec2:DeleteNetworkInterface\",\"ec2:CreateNetworkInterface\",\"ec2:AttachNetworkInterface\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:ec2:eu-west-1:899076912694:subnet/subnet-0a8409260cbaf999f\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0cb505f744b1c74eb\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0aa6fd5972038141a\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-09096e91dd18fa7d4\",\"arn:aws:ec2:eu-west-1:899076912694:security-group/sg-032c47f80254c35c7\",\"arn:aws:ec2:eu-west-1:899076912694:network-interface/*\"],\"Sid\":\"EC2Modify\"},{\"Action\":[\"glue:GetConnections\",\"glue:GetConnection\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:connection/eniaws-glue-euwe1-ictd-899076912694-job-l1-l2\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"],\"Sid\":\"GlueConnectionRead\"},{\"Action\":[\"ec2:DescribeVpcs\",\"ec2:DescribeVpcEndpoints\",\"ec2:DescribeSubnets\",\"ec2:DescribeSecurityGroups\",\"ec2:DescribeRouteTables\",\"ec2:DescribeNetworkInterfaces\"],\"Effect\":\"Allow\",\"Resource\":\"*\",\"Sid\":\"EC2DescribeForGlueNetwork\"},{\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\",\"Sid\":\"AllowRestrictedGlueActions\"},{\"Action\":[\"logs:DisassociateKmsKey\",\"logs:AssociateKmsKey\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/*\",\"arn:aws:kms:eu-west-1:899076912694:alias/aws/glue\"],\"Sid\":\"AllowCloudWatchLogsAssociateKmsKey\"}]}",
                      "role": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2"
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_job_2.aws_glue_connection.network",
                      "module.bb_blueprint.module.glue_job_2.aws_iam_role.role",
                      "module.bb_blueprint.module.glue_job_2.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.glue_job_2.data.aws_iam_policy_document.custom_iam_policy_document",
                      "module.bb_blueprint.module.glue_job_2.data.aws_iam_policy_document.glue_job_combined_policy",
                      "module.bb_blueprint.module.glue_job_2.data.aws_iam_policy_document.glue_job_policy",
                      "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket.s3_bucket"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "name": "glue_job_permissions",
                      "role": "eniaws-glue-job-role-euwe1-ictd-899076912694-job-l1-l2"
                    }
                  }
                ],
                "address": "module.bb_blueprint.module.glue_job_2"
              },
              {
                "resources": [
                  {
                    "address": "module.bb_blueprint.module.lambda_trigger.aws_iam_role.role",
                    "mode": "managed",
                    "type": "aws_iam_role",
                    "name": "role",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:iam::899076912694:role/bb-lambda-alfa-test_execution_role",
                      "assume_role_policy": "{\"Statement\":[{\"Action\":\"sts:AssumeRole\",\"Effect\":\"Allow\",\"Principal\":{\"Service\":\"lambda.amazonaws.com\"}}],\"Version\":\"2012-10-17\"}",
                      "create_date": "2026-02-12T09:35:19Z",
                      "description": "",
                      "force_detach_policies": false,
                      "id": "bb-lambda-alfa-test_execution_role",
                      "inline_policy": [
                        {
                          "name": "lambda_permissions",
                          "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:logs:*:*:*\",\"Sid\":\"AllowBasicLambdaExecution\"},{\"Action\":\"states:StartExecution\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/*\",\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"],\"Sid\":\"AllowLambdaAccessToStepFunction\"},{\"Action\":[\"s3:PutObject\",\"s3:GetObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/*\",\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"],\"Sid\":\"AllowS3InvokeLambda\"}]}"
                        }
                      ],
                      "managed_policy_arns": [
                        "arn:aws:iam::aws:policy/service-role/AWSLambdaVPCAccessExecutionRole"
                      ],
                      "max_session_duration": 3600,
                      "name": "bb-lambda-alfa-test_execution_role",
                      "name_prefix": "",
                      "path": "/",
                      "permissions_boundary": "arn:aws:iam::899076912694:policy/eniaws-ply-icth-iamboundary_for_vended_sscoped_service_accounts",
                      "tags": {},
                      "tags_all": {},
                      "unique_id": "AROA5CVJI6Y3OUVC5LMMM"
                    },
                    "sensitive_values": {
                      "inline_policy": [
                        {}
                      ],
                      "managed_policy_arns": [
                        false
                      ],
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.assume_role"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "name": "bb-lambda-alfa-test_execution_role"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.lambda_trigger.aws_iam_role_policy.lambda_permissions",
                    "mode": "managed",
                    "type": "aws_iam_role_policy",
                    "name": "lambda_permissions",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "bb-lambda-alfa-test_execution_role:lambda_permissions",
                      "name": "lambda_permissions",
                      "name_prefix": "",
                      "policy": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Effect\":\"Allow\",\"Resource\":\"arn:aws:logs:*:*:*\",\"Sid\":\"AllowBasicLambdaExecution\"},{\"Action\":\"states:StartExecution\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/*\",\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"],\"Sid\":\"AllowLambdaAccessToStepFunction\"},{\"Action\":[\"s3:PutObject\",\"s3:GetObject\"],\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/*\",\"arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test\"],\"Sid\":\"AllowS3InvokeLambda\"}]}",
                      "role": "bb-lambda-alfa-test_execution_role"
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.aws_cloudwatch_log_group.sf_logs",
                      "module.bb_blueprint.aws_cloudwatch_log_resource_policy.allow_sfn",
                      "module.bb_blueprint.aws_iam_role.step_function_role",
                      "module.bb_blueprint.aws_kms_key.logs",
                      "module.bb_blueprint.aws_sfn_state_machine.step_function",
                      "module.bb_blueprint.aws_sns_topic.error_notification",
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.glue_job_1.aws_glue_connection.network",
                      "module.bb_blueprint.module.glue_job_1.aws_glue_job.job",
                      "module.bb_blueprint.module.glue_job_1.aws_glue_security_configuration.this",
                      "module.bb_blueprint.module.glue_job_1.aws_iam_role.role",
                      "module.bb_blueprint.module.glue_job_1.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.glue_job_2.aws_glue_connection.network",
                      "module.bb_blueprint.module.glue_job_2.aws_glue_job.job",
                      "module.bb_blueprint.module.glue_job_2.aws_glue_security_configuration.this",
                      "module.bb_blueprint.module.glue_job_2.aws_iam_role.role",
                      "module.bb_blueprint.module.glue_job_2.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.lambda_trigger.aws_iam_role.role",
                      "module.bb_blueprint.module.lambda_trigger.aws_lambda_function.func",
                      "module.bb_blueprint.module.lambda_trigger.aws_security_group.lambdansg",
                      "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.combined",
                      "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.custom_lambda_permissions",
                      "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.lambda_permissions",
                      "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "name": "lambda_permissions",
                      "role": "bb-lambda-alfa-test_execution_role"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.lambda_trigger.aws_iam_role_policy_attachment.lambda_vpc_access",
                    "mode": "managed",
                    "type": "aws_iam_role_policy_attachment",
                    "name": "lambda_vpc_access",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "bb-lambda-alfa-test_execution_role/arn:aws:iam::aws:policy/service-role/AWSLambdaVPCAccessExecutionRole",
                      "policy_arn": "arn:aws:iam::aws:policy/service-role/AWSLambdaVPCAccessExecutionRole",
                      "role": "bb-lambda-alfa-test_execution_role"
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.module.lambda_trigger.aws_iam_role.role",
                      "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.assume_role"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "policy_arn": "arn:aws:iam::aws:policy/service-role/AWSLambdaVPCAccessExecutionRole",
                      "role": "bb-lambda-alfa-test_execution_role"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.lambda_trigger.aws_lambda_function.func",
                    "mode": "managed",
                    "type": "aws_lambda_function",
                    "name": "func",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "architectures": [
                        "x86_64"
                      ],
                      "arn": "arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
                      "capacity_provider_config": [],
                      "code_sha256": "wEM5Bj4bYOvtHlAqd749iee2e/+quXoveiBpRpv51/Q=",
                      "code_signing_config_arn": "",
                      "dead_letter_config": [],
                      "description": "",
                      "durable_config": [],
                      "environment": [
                        {
                          "variables": {
                            "BUCKET_L0_ID": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                            "CONFIG1": "valore1",
                            "CONFIG2": "valore2",
                            "CONFIG3": "valore3",
                            "FUNCTIONVERSION": "2db4a82d",
                            "MYENV": "sd"
                          }
                        }
                      ],
                      "ephemeral_storage": [
                        {
                          "size": 512
                        }
                      ],
                      "file_system_config": [],
                      "filename": ".terraform/modules/bb_blueprint.lambda_trigger/lambda/function.zip",
                      "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
                      "handler": "pdf_to_csv.handler.lambda_handler",
                      "id": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
                      "image_config": [],
                      "image_uri": "",
                      "invoke_arn": "arn:aws:apigateway:eu-west-1:lambda:path/2015-03-31/functions/arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/invocations",
                      "kms_key_arn": "",
                      "last_modified": "2026-02-13T14:56:56.000+0000",
                      "layers": [],
                      "logging_config": [
                        {
                          "application_log_level": "",
                          "log_format": "Text",
                          "log_group": "/aws/lambda/eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
                          "system_log_level": ""
                        }
                      ],
                      "memory_size": 256,
                      "package_type": "Zip",
                      "publish": false,
                      "publish_to": null,
                      "qualified_arn": "arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test:$LATEST",
                      "qualified_invoke_arn": "arn:aws:apigateway:eu-west-1:lambda:path/2015-03-31/functions/arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test:$LATEST/invocations",
                      "region": "eu-west-1",
                      "replace_security_groups_on_destroy": null,
                      "replacement_security_group_ids": null,
                      "reserved_concurrent_executions": -1,
                      "response_streaming_invoke_arn": "arn:aws:apigateway:eu-west-1:lambda:path/2021-11-15/functions/arn:aws:lambda:eu-west-1:899076912694:function:eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test/response-streaming-invocations",
                      "role": "arn:aws:iam::899076912694:role/bb-lambda-alfa-test_execution_role",
                      "runtime": "python3.12",
                      "s3_bucket": null,
                      "s3_key": null,
                      "s3_object_version": null,
                      "signing_job_arn": "",
                      "signing_profile_version_arn": "",
                      "skip_destroy": false,
                      "snap_start": [],
                      "source_code_hash": "",
                      "source_code_size": 28895990,
                      "source_kms_key_arn": "",
                      "tags": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "lambda",
                        "BuildingBlockVersion": "1.0.1",
                        "Env": "sd",
                        "Name": "lambda"
                      },
                      "tags_all": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "lambda",
                        "BuildingBlockVersion": "1.0.1",
                        "Env": "sd",
                        "Name": "lambda"
                      },
                      "tenancy_config": [],
                      "timeout": 3,
                      "timeouts": null,
                      "tracing_config": [
                        {
                          "mode": "Active"
                        }
                      ],
                      "version": "$LATEST",
                      "vpc_config": [
                        {
                          "ipv6_allowed_for_dual_stack": false,
                          "security_group_ids": [
                            "sg-0050539b6cdca740b"
                          ],
                          "subnet_ids": [
                            "subnet-0bbf991ef124badcc",
                            "subnet-0c4e308d22ad05ee7"
                          ],
                          "vpc_id": "vpc-07dd8497864cf1073"
                        }
                      ]
                    },
                    "sensitive_values": {
                      "architectures": [
                        false
                      ],
                      "capacity_provider_config": [],
                      "dead_letter_config": [],
                      "durable_config": [],
                      "environment": [
                        {
                          "variables": {}
                        }
                      ],
                      "ephemeral_storage": [
                        {}
                      ],
                      "file_system_config": [],
                      "image_config": [],
                      "layers": [],
                      "logging_config": [
                        {}
                      ],
                      "snap_start": [],
                      "tags": {},
                      "tags_all": {},
                      "tenancy_config": [],
                      "tracing_config": [
                        {}
                      ],
                      "vpc_config": [
                        {
                          "security_group_ids": [
                            false
                          ],
                          "subnet_ids": [
                            false,
                            false
                          ]
                        }
                      ]
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.lambda_trigger.aws_iam_role.role",
                      "module.bb_blueprint.module.lambda_trigger.aws_security_group.lambdansg",
                      "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.assume_role"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.lambda_trigger.aws_lambda_function_event_invoke_config.error_destination",
                    "mode": "managed",
                    "type": "aws_lambda_function_event_invoke_config",
                    "name": "error_destination",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "destination_config": [],
                      "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
                      "id": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
                      "maximum_event_age_in_seconds": 0,
                      "maximum_retry_attempts": 2,
                      "qualifier": "",
                      "region": "eu-west-1"
                    },
                    "sensitive_values": {
                      "destination_config": []
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.lambda_trigger.aws_iam_role.role",
                      "module.bb_blueprint.module.lambda_trigger.aws_lambda_function.func",
                      "module.bb_blueprint.module.lambda_trigger.aws_security_group.lambdansg",
                      "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.assume_role"
                    ]
                  },
                  {
                    "address": "module.bb_blueprint.module.lambda_trigger.aws_lambda_permission.resource_permission[\"eni-s3-lambda-trigger-permission-dpf-bp-dp1453\"]",
                    "mode": "managed",
                    "type": "aws_lambda_permission",
                    "name": "resource_permission",
                    "index": "eni-s3-lambda-trigger-permission-dpf-bp-dp1453",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "action": "lambda:InvokeFunction",
                      "event_source_token": "",
                      "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
                      "function_url_auth_type": "",
                      "id": "eni-s3-lambda-trigger-permission-dpf-bp-dp1453",
                      "invoked_via_function_url": null,
                      "principal": "s3.amazonaws.com",
                      "principal_org_id": "",
                      "qualifier": "",
                      "region": "eu-west-1",
                      "source_account": "899076912694",
                      "source_arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "statement_id": "eni-s3-lambda-trigger-permission-dpf-bp-dp1453",
                      "statement_id_prefix": ""
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.lambda_trigger.aws_iam_role.role",
                      "module.bb_blueprint.module.lambda_trigger.aws_lambda_function.func",
                      "module.bb_blueprint.module.lambda_trigger.aws_security_group.lambdansg",
                      "module.bb_blueprint.module.lambda_trigger.data.aws_iam_policy_document.assume_role",
                      "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "function_name": "eniaws-lmb-euwe1-ictd-bb-lambda-alfa-test",
                      "qualifier": null,
                      "region": "eu-west-1",
                      "statement_id": "eni-s3-lambda-trigger-permission-dpf-bp-dp1453"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.lambda_trigger.aws_security_group.lambdansg",
                    "mode": "managed",
                    "type": "aws_security_group",
                    "name": "lambdansg",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 1,
                    "values": {
                      "arn": "arn:aws:ec2:eu-west-1:899076912694:security-group/sg-0050539b6cdca740b",
                      "description": "Security group for Lambda function",
                      "egress": [],
                      "id": "sg-0050539b6cdca740b",
                      "ingress": [],
                      "name": "bb-lambda-alfa-test_sg",
                      "name_prefix": "",
                      "owner_id": "899076912694",
                      "region": "eu-west-1",
                      "revoke_rules_on_delete": false,
                      "tags": {},
                      "tags_all": {},
                      "timeouts": null,
                      "vpc_id": "vpc-07dd8497864cf1073"
                    },
                    "sensitive_values": {
                      "egress": [],
                      "ingress": [],
                      "tags": {},
                      "tags_all": {}
                    },
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "id": "sg-0050539b6cdca740b",
                      "region": "eu-west-1"
                    }
                  }
                ],
                "address": "module.bb_blueprint.module.lambda_trigger"
              },
              {
                "resources": [
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_iam_policy.iam_policy[\"0\"]",
                    "mode": "managed",
                    "type": "aws_iam_policy",
                    "name": "iam_policy",
                    "index": "0",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-artifacts",
                      "attachment_count": 0,
                      "delay_after_policy_creation_in_ms": null,
                      "description": "",
                      "id": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-artifacts",
                      "name": "policy_0_dpf-bp-dp1453-artifacts",
                      "name_prefix": "",
                      "path": "/",
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-artifacts\"],\"Sid\":\"AllowAllS3ArtifactActions\"}],\"Version\":\"2012-10-17\"}",
                      "policy_id": "ANPA5CVJI6Y3PNJ4FZDNA",
                      "tags": {},
                      "tags_all": {}
                    },
                    "sensitive_values": {
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.custom_iam_policy_document"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-artifacts"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket",
                    "mode": "managed",
                    "type": "aws_s3_bucket",
                    "name": "s3_bucket",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "acceleration_status": "",
                      "acl": null,
                      "arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "bucket_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts.s3.amazonaws.com",
                      "bucket_prefix": "",
                      "bucket_region": "eu-west-1",
                      "bucket_regional_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts.s3.eu-west-1.amazonaws.com",
                      "cors_rule": [],
                      "force_destroy": true,
                      "grant": [
                        {
                          "id": "d1feaac8a6ab06d21b99eb178e911dfdf5749f1c6a32504e3b10308ba58bfa01",
                          "permissions": [
                            "FULL_CONTROL"
                          ],
                          "type": "CanonicalUser",
                          "uri": ""
                        }
                      ],
                      "hosted_zone_id": "Z1BKCTXD74EZPE",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "lifecycle_rule": [],
                      "logging": [
                        {
                          "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                          "target_prefix": "log/"
                        }
                      ],
                      "object_lock_configuration": [],
                      "object_lock_enabled": false,
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
                      "region": "eu-west-1",
                      "replication_configuration": [],
                      "request_payer": "BucketOwner",
                      "server_side_encryption_configuration": [
                        {
                          "rule": [
                            {
                              "apply_server_side_encryption_by_default": [
                                {
                                  "kms_master_key_id": "",
                                  "sse_algorithm": "AES256"
                                }
                              ],
                              "bucket_key_enabled": false
                            }
                          ]
                        }
                      ],
                      "tags": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "s3",
                        "BuildingBlockVersion": "1.1.0",
                        "Env": "sd",
                        "Name": "s3_artifacts"
                      },
                      "tags_all": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "s3",
                        "BuildingBlockVersion": "1.1.0",
                        "Env": "sd",
                        "Name": "s3_artifacts"
                      },
                      "timeouts": null,
                      "versioning": [
                        {
                          "enabled": false,
                          "mfa_delete": false
                        }
                      ],
                      "website": [],
                      "website_domain": null,
                      "website_endpoint": null
                    },
                    "sensitive_values": {
                      "cors_rule": [],
                      "grant": [
                        {
                          "permissions": [
                            false
                          ]
                        }
                      ],
                      "lifecycle_rule": [],
                      "logging": [
                        {}
                      ],
                      "object_lock_configuration": [],
                      "replication_configuration": [],
                      "server_side_encryption_configuration": [
                        {
                          "rule": [
                            {
                              "apply_server_side_encryption_by_default": [
                                {}
                              ]
                            }
                          ]
                        }
                      ],
                      "tags": {},
                      "tags_all": {},
                      "versioning": [
                        {}
                      ],
                      "website": []
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket_logging.example",
                    "mode": "managed",
                    "type": "aws_s3_bucket_logging",
                    "name": "example",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "expected_bucket_owner": "",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "region": "eu-west-1",
                      "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                      "target_grant": [],
                      "target_object_key_format": [
                        {
                          "partitioned_prefix": [
                            {
                              "partition_date_source": "EventTime"
                            }
                          ],
                          "simple_prefix": []
                        }
                      ],
                      "target_prefix": "log/"
                    },
                    "sensitive_values": {
                      "target_grant": [],
                      "target_object_key_format": [
                        {
                          "partitioned_prefix": [
                            {}
                          ],
                          "simple_prefix": []
                        }
                      ]
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_s3_bucket.bucket_s3_access_logs"
                    ],
                    "identity_schema_version": 1,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket_policy.bucket_policy",
                    "mode": "managed",
                    "type": "aws_s3_bucket_policy",
                    "name": "bucket_policy",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
                      "region": "eu-west-1"
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.allow_prisma",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.allow_prisma_object",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.allow_public_through_f5",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.allow_ssl_only",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.allow_vpc_source",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.combined",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.combined_custom",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.custom_policy_document",
                      "module.bb_blueprint.module.s3_buckets_artifacts.data.aws_iam_policy_document.deny_not_principals"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket_public_access_block.public_access_block",
                    "mode": "managed",
                    "type": "aws_s3_bucket_public_access_block",
                    "name": "public_access_block",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "block_public_acls": true,
                      "block_public_policy": true,
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "ignore_public_acls": true,
                      "region": "eu-west-1",
                      "restrict_public_buckets": true,
                      "skip_destroy": null
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_artifacts.aws_s3_bucket.s3_bucket"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-artifacts",
                      "region": "eu-west-1"
                    }
                  }
                ],
                "address": "module.bb_blueprint.module.s3_buckets_artifacts"
              },
              {
                "resources": [
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l0.aws_iam_policy.iam_policy[\"0\"]",
                    "mode": "managed",
                    "type": "aws_iam_policy",
                    "name": "iam_policy",
                    "index": "0",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l0",
                      "attachment_count": 0,
                      "delay_after_policy_creation_in_ms": null,
                      "description": "",
                      "id": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l0",
                      "name": "policy_0_dpf-bp-dp1453-l0",
                      "name_prefix": "",
                      "path": "/",
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0\"],\"Sid\":\"AllowAllS3L0Actions\"}],\"Version\":\"2012-10-17\"}",
                      "policy_id": "ANPA5CVJI6Y3AHELZJF5F",
                      "tags": {},
                      "tags_all": {}
                    },
                    "sensitive_values": {
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.custom_iam_policy_document"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l0"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket",
                    "mode": "managed",
                    "type": "aws_s3_bucket",
                    "name": "s3_bucket",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "acceleration_status": "",
                      "acl": null,
                      "arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "bucket_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0.s3.amazonaws.com",
                      "bucket_prefix": "",
                      "bucket_region": "eu-west-1",
                      "bucket_regional_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0.s3.eu-west-1.amazonaws.com",
                      "cors_rule": [],
                      "force_destroy": true,
                      "grant": [
                        {
                          "id": "d1feaac8a6ab06d21b99eb178e911dfdf5749f1c6a32504e3b10308ba58bfa01",
                          "permissions": [
                            "FULL_CONTROL"
                          ],
                          "type": "CanonicalUser",
                          "uri": ""
                        }
                      ],
                      "hosted_zone_id": "Z1BKCTXD74EZPE",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "lifecycle_rule": [],
                      "logging": [
                        {
                          "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                          "target_prefix": "log/"
                        }
                      ],
                      "object_lock_configuration": [],
                      "object_lock_enabled": false,
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
                      "region": "eu-west-1",
                      "replication_configuration": [],
                      "request_payer": "BucketOwner",
                      "server_side_encryption_configuration": [
                        {
                          "rule": [
                            {
                              "apply_server_side_encryption_by_default": [
                                {
                                  "kms_master_key_id": "",
                                  "sse_algorithm": "AES256"
                                }
                              ],
                              "bucket_key_enabled": false
                            }
                          ]
                        }
                      ],
                      "tags": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "s3",
                        "BuildingBlockVersion": "1.1.0",
                        "Env": "sd",
                        "Name": "s3_l0"
                      },
                      "tags_all": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "s3",
                        "BuildingBlockVersion": "1.1.0",
                        "Env": "sd",
                        "Name": "s3_l0"
                      },
                      "timeouts": null,
                      "versioning": [
                        {
                          "enabled": false,
                          "mfa_delete": false
                        }
                      ],
                      "website": [],
                      "website_domain": null,
                      "website_endpoint": null
                    },
                    "sensitive_values": {
                      "cors_rule": [],
                      "grant": [
                        {
                          "permissions": [
                            false
                          ]
                        }
                      ],
                      "lifecycle_rule": [],
                      "logging": [
                        {}
                      ],
                      "object_lock_configuration": [],
                      "replication_configuration": [],
                      "server_side_encryption_configuration": [
                        {
                          "rule": [
                            {
                              "apply_server_side_encryption_by_default": [
                                {}
                              ]
                            }
                          ]
                        }
                      ],
                      "tags": {},
                      "tags_all": {},
                      "versioning": [
                        {}
                      ],
                      "website": []
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket_logging.example",
                    "mode": "managed",
                    "type": "aws_s3_bucket_logging",
                    "name": "example",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "expected_bucket_owner": "",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "region": "eu-west-1",
                      "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                      "target_grant": [],
                      "target_object_key_format": [
                        {
                          "partitioned_prefix": [
                            {
                              "partition_date_source": "EventTime"
                            }
                          ],
                          "simple_prefix": []
                        }
                      ],
                      "target_prefix": "log/"
                    },
                    "sensitive_values": {
                      "target_grant": [],
                      "target_object_key_format": [
                        {
                          "partitioned_prefix": [
                            {}
                          ],
                          "simple_prefix": []
                        }
                      ]
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_s3_bucket.bucket_s3_access_logs"
                    ],
                    "identity_schema_version": 1,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket_policy.bucket_policy",
                    "mode": "managed",
                    "type": "aws_s3_bucket_policy",
                    "name": "bucket_policy",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
                      "region": "eu-west-1"
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.allow_prisma",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.allow_prisma_object",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.allow_public_through_f5",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.allow_ssl_only",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.allow_vpc_source",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.combined",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.combined_custom",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.custom_policy_document",
                      "module.bb_blueprint.module.s3_buckets_l0.data.aws_iam_policy_document.deny_not_principals"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket_public_access_block.public_access_block",
                    "mode": "managed",
                    "type": "aws_s3_bucket_public_access_block",
                    "name": "public_access_block",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "block_public_acls": true,
                      "block_public_policy": true,
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "ignore_public_acls": true,
                      "region": "eu-west-1",
                      "restrict_public_buckets": true,
                      "skip_destroy": null
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l0.aws_s3_bucket.s3_bucket"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l0",
                      "region": "eu-west-1"
                    }
                  }
                ],
                "address": "module.bb_blueprint.module.s3_buckets_l0"
              },
              {
                "resources": [
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l1.aws_iam_policy.iam_policy[\"0\"]",
                    "mode": "managed",
                    "type": "aws_iam_policy",
                    "name": "iam_policy",
                    "index": "0",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l1",
                      "attachment_count": 0,
                      "delay_after_policy_creation_in_ms": null,
                      "description": "",
                      "id": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l1",
                      "name": "policy_0_dpf-bp-dp1453-l1",
                      "name_prefix": "",
                      "path": "/",
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l1\"],\"Sid\":\"AllowAllS3L1Actions\"}],\"Version\":\"2012-10-17\"}",
                      "policy_id": "ANPA5CVJI6Y3FWMV62TFZ",
                      "tags": {},
                      "tags_all": {}
                    },
                    "sensitive_values": {
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.custom_iam_policy_document"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket.s3_bucket",
                    "mode": "managed",
                    "type": "aws_s3_bucket",
                    "name": "s3_bucket",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "acceleration_status": "",
                      "acl": null,
                      "arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "bucket_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1.s3.amazonaws.com",
                      "bucket_prefix": "",
                      "bucket_region": "eu-west-1",
                      "bucket_regional_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1.s3.eu-west-1.amazonaws.com",
                      "cors_rule": [],
                      "force_destroy": true,
                      "grant": [
                        {
                          "id": "d1feaac8a6ab06d21b99eb178e911dfdf5749f1c6a32504e3b10308ba58bfa01",
                          "permissions": [
                            "FULL_CONTROL"
                          ],
                          "type": "CanonicalUser",
                          "uri": ""
                        }
                      ],
                      "hosted_zone_id": "Z1BKCTXD74EZPE",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "lifecycle_rule": [],
                      "logging": [
                        {
                          "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                          "target_prefix": "log/"
                        }
                      ],
                      "object_lock_configuration": [],
                      "object_lock_enabled": false,
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
                      "region": "eu-west-1",
                      "replication_configuration": [],
                      "request_payer": "BucketOwner",
                      "server_side_encryption_configuration": [
                        {
                          "rule": [
                            {
                              "apply_server_side_encryption_by_default": [
                                {
                                  "kms_master_key_id": "",
                                  "sse_algorithm": "AES256"
                                }
                              ],
                              "bucket_key_enabled": false
                            }
                          ]
                        }
                      ],
                      "tags": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "s3",
                        "BuildingBlockVersion": "1.1.0",
                        "Env": "sd",
                        "Name": "s3_l1"
                      },
                      "tags_all": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "s3",
                        "BuildingBlockVersion": "1.1.0",
                        "Env": "sd",
                        "Name": "s3_l1"
                      },
                      "timeouts": null,
                      "versioning": [
                        {
                          "enabled": false,
                          "mfa_delete": false
                        }
                      ],
                      "website": [],
                      "website_domain": null,
                      "website_endpoint": null
                    },
                    "sensitive_values": {
                      "cors_rule": [],
                      "grant": [
                        {
                          "permissions": [
                            false
                          ]
                        }
                      ],
                      "lifecycle_rule": [],
                      "logging": [
                        {}
                      ],
                      "object_lock_configuration": [],
                      "replication_configuration": [],
                      "server_side_encryption_configuration": [
                        {
                          "rule": [
                            {
                              "apply_server_side_encryption_by_default": [
                                {}
                              ]
                            }
                          ]
                        }
                      ],
                      "tags": {},
                      "tags_all": {},
                      "versioning": [
                        {}
                      ],
                      "website": []
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket_logging.example",
                    "mode": "managed",
                    "type": "aws_s3_bucket_logging",
                    "name": "example",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "expected_bucket_owner": "",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "region": "eu-west-1",
                      "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                      "target_grant": [],
                      "target_object_key_format": [
                        {
                          "partitioned_prefix": [
                            {
                              "partition_date_source": "EventTime"
                            }
                          ],
                          "simple_prefix": []
                        }
                      ],
                      "target_prefix": "log/"
                    },
                    "sensitive_values": {
                      "target_grant": [],
                      "target_object_key_format": [
                        {
                          "partitioned_prefix": [
                            {}
                          ],
                          "simple_prefix": []
                        }
                      ]
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_s3_bucket.bucket_s3_access_logs"
                    ],
                    "identity_schema_version": 1,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket_policy.bucket_policy",
                    "mode": "managed",
                    "type": "aws_s3_bucket_policy",
                    "name": "bucket_policy",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
                      "region": "eu-west-1"
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.allow_prisma",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.allow_prisma_object",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.allow_public_through_f5",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.allow_ssl_only",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.allow_vpc_source",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.combined",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.combined_custom",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.custom_policy_document",
                      "module.bb_blueprint.module.s3_buckets_l1.data.aws_iam_policy_document.deny_not_principals"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket_public_access_block.public_access_block",
                    "mode": "managed",
                    "type": "aws_s3_bucket_public_access_block",
                    "name": "public_access_block",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "block_public_acls": true,
                      "block_public_policy": true,
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "ignore_public_acls": true,
                      "region": "eu-west-1",
                      "restrict_public_buckets": true,
                      "skip_destroy": null
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l1.aws_s3_bucket.s3_bucket"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l1",
                      "region": "eu-west-1"
                    }
                  }
                ],
                "address": "module.bb_blueprint.module.s3_buckets_l1"
              },
              {
                "resources": [
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l2.aws_iam_policy.iam_policy[\"0\"]",
                    "mode": "managed",
                    "type": "aws_iam_policy",
                    "name": "iam_policy",
                    "index": "0",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l2",
                      "attachment_count": 0,
                      "delay_after_policy_creation_in_ms": null,
                      "description": "",
                      "id": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l2",
                      "name": "policy_0_dpf-bp-dp1453-l2",
                      "name_prefix": "",
                      "path": "/",
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Effect\":\"Allow\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l1/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l1\"],\"Sid\":\"AllowAllS3L2Actions\"}],\"Version\":\"2012-10-17\"}",
                      "policy_id": "ANPA5CVJI6Y3MI4AZWR42",
                      "tags": {},
                      "tags_all": {}
                    },
                    "sensitive_values": {
                      "tags": {},
                      "tags_all": {}
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.custom_iam_policy_document"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "arn": "arn:aws:iam::899076912694:policy/policy_0_dpf-bp-dp1453-l2"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket.s3_bucket",
                    "mode": "managed",
                    "type": "aws_s3_bucket",
                    "name": "s3_bucket",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "acceleration_status": "",
                      "acl": null,
                      "arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "bucket_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2.s3.amazonaws.com",
                      "bucket_prefix": "",
                      "bucket_region": "eu-west-1",
                      "bucket_regional_domain_name": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2.s3.eu-west-1.amazonaws.com",
                      "cors_rule": [],
                      "force_destroy": true,
                      "grant": [
                        {
                          "id": "d1feaac8a6ab06d21b99eb178e911dfdf5749f1c6a32504e3b10308ba58bfa01",
                          "permissions": [
                            "FULL_CONTROL"
                          ],
                          "type": "CanonicalUser",
                          "uri": ""
                        }
                      ],
                      "hosted_zone_id": "Z1BKCTXD74EZPE",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "lifecycle_rule": [],
                      "logging": [
                        {
                          "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                          "target_prefix": "log/"
                        }
                      ],
                      "object_lock_configuration": [],
                      "object_lock_enabled": false,
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
                      "region": "eu-west-1",
                      "replication_configuration": [],
                      "request_payer": "BucketOwner",
                      "server_side_encryption_configuration": [
                        {
                          "rule": [
                            {
                              "apply_server_side_encryption_by_default": [
                                {
                                  "kms_master_key_id": "",
                                  "sse_algorithm": "AES256"
                                }
                              ],
                              "bucket_key_enabled": false
                            }
                          ]
                        }
                      ],
                      "tags": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "s3",
                        "BuildingBlockVersion": "1.1.0",
                        "Env": "sd",
                        "Name": "s3_l2"
                      },
                      "tags_all": {
                        "ApplicationID": "2102",
                        "ApplicationName": "DATA PLATFORM FOUNDATION",
                        "BuildingBlockName": "s3",
                        "BuildingBlockVersion": "1.1.0",
                        "Env": "sd",
                        "Name": "s3_l2"
                      },
                      "timeouts": null,
                      "versioning": [
                        {
                          "enabled": false,
                          "mfa_delete": false
                        }
                      ],
                      "website": [],
                      "website_domain": null,
                      "website_endpoint": null
                    },
                    "sensitive_values": {
                      "cors_rule": [],
                      "grant": [
                        {
                          "permissions": [
                            false
                          ]
                        }
                      ],
                      "lifecycle_rule": [],
                      "logging": [
                        {}
                      ],
                      "object_lock_configuration": [],
                      "replication_configuration": [],
                      "server_side_encryption_configuration": [
                        {
                          "rule": [
                            {
                              "apply_server_side_encryption_by_default": [
                                {}
                              ]
                            }
                          ]
                        }
                      ],
                      "tags": {},
                      "tags_all": {},
                      "versioning": [
                        {}
                      ],
                      "website": []
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket_logging.example",
                    "mode": "managed",
                    "type": "aws_s3_bucket_logging",
                    "name": "example",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "expected_bucket_owner": "",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "region": "eu-west-1",
                      "target_bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                      "target_grant": [],
                      "target_object_key_format": [
                        {
                          "partitioned_prefix": [
                            {
                              "partition_date_source": "EventTime"
                            }
                          ],
                          "simple_prefix": []
                        }
                      ],
                      "target_prefix": "log/"
                    },
                    "sensitive_values": {
                      "target_grant": [],
                      "target_object_key_format": [
                        {
                          "partitioned_prefix": [
                            {}
                          ],
                          "simple_prefix": []
                        }
                      ]
                    },
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_s3_bucket.bucket_s3_access_logs"
                    ],
                    "identity_schema_version": 1,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket_policy.bucket_policy",
                    "mode": "managed",
                    "type": "aws_s3_bucket_policy",
                    "name": "bucket_policy",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "policy": "{\"Statement\":[{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowSSLOnlyAsInputPolicy\"},{\"Action\":[\"s3:ListBucket\",\"s3:GetReplicationConfiguration\",\"s3:GetMetricsConfiguration\",\"s3:GetLifecycleConfiguration\",\"s3:GetInventoryConfiguration\",\"s3:GetEncryptionConfiguration\",\"s3:GetBucketWebsite\",\"s3:GetBucketVersioning\",\"s3:GetBucketTagging\",\"s3:GetBucketPublicAccessBlock\",\"s3:GetBucketPolicyStatus\",\"s3:GetBucketPolicy\",\"s3:GetBucketOwnershipControls\",\"s3:GetBucketObjectLockConfiguration\",\"s3:GetBucketLogging\",\"s3:GetBucketLocation\",\"s3:GetBucketCORS\",\"s3:GetBucketAcl\",\"s3:GetBucket*\",\"s3:GetAnalyticsConfiguration\",\"s3:GetAccelerateConfiguration\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\",\"Sid\":\"AllowPrisma\"},{\"Action\":[\"s3:GetObjectVersionAcl\",\"s3:GetObjectTagging\",\"s3:GetObjectAcl\"],\"Effect\":\"Allow\",\"Principal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"Sid\":\"AllowPrismaObject\"},{\"Action\":\"s3:*\",\"Condition\":{\"BoolIfExists\":{\"aws:PrincipalIsAWSService\":\"false\"},\"NotIpAddress\":{\"aws:VpcSourceIp\":[\"10.68.98.160/27\",\"10.68.98.128/27\"]},\"StringNotEquals\":{\"aws:PrincipalArn\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\",\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Deny\",\"NotPrincipal\":{\"AWS\":\"arn:aws:iam::899076912694:role/PrismaCloudRole-Onboarding-member\"},\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"DenyNotPrincipals\"},{\"Action\":\"s3:*\",\"Condition\":{\"Bool\":{\"aws:SecureTransport\":\"false\"}},\"Effect\":\"Deny\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowSSLOnly\"},{\"Action\":\"s3:*\",\"Condition\":{\"StringEquals\":{\"aws:VpceAccount\":\"638883080465\"}},\"Effect\":\"Allow\",\"Principal\":\"*\",\"Resource\":[\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2/*\",\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2\"],\"Sid\":\"AllowActionsFromInsideVPC\"}],\"Version\":\"2012-10-17\"}",
                      "region": "eu-west-1"
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket.s3_bucket",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.allow_prisma",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.allow_prisma_object",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.allow_public_through_f5",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.allow_ssl_only",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.allow_vpc_source",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.combined",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.combined_custom",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.custom_policy_document",
                      "module.bb_blueprint.module.s3_buckets_l2.data.aws_iam_policy_document.deny_not_principals"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "region": "eu-west-1"
                    }
                  },
                  {
                    "address": "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket_public_access_block.public_access_block",
                    "mode": "managed",
                    "type": "aws_s3_bucket_public_access_block",
                    "name": "public_access_block",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "block_public_acls": true,
                      "block_public_policy": true,
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "ignore_public_acls": true,
                      "region": "eu-west-1",
                      "restrict_public_buckets": true,
                      "skip_destroy": null
                    },
                    "sensitive_values": {},
                    "depends_on": [
                      "module.bb_blueprint.data.aws_caller_identity.current",
                      "module.bb_blueprint.data.aws_region.current",
                      "module.bb_blueprint.module.s3_buckets_l2.aws_s3_bucket.s3_bucket"
                    ],
                    "identity_schema_version": 0,
                    "identity": {
                      "account_id": "899076912694",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-dpf-bp-dp1453-l2",
                      "region": "eu-west-1"
                    }
                  }
                ],
                "address": "module.bb_blueprint.module.s3_buckets_l2"
              }
            ]
          },
          {
            "resources": [
              {
                "address": "module.blueprint.data.aws_caller_identity.current",
                "mode": "data",
                "type": "aws_caller_identity",
                "name": "current",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "account_id": "899076912694",
                  "arn": "arn:aws:iam::899076912694:user/eniaws-sa-ictd-2102_pscoped_01",
                  "id": "899076912694",
                  "user_id": "AIDA5CVJI6Y3ARMQZ2JO3"
                },
                "sensitive_values": {}
              },
              {
                "address": "module.blueprint.data.aws_region.current",
                "mode": "data",
                "type": "aws_region",
                "name": "current",
                "provider_name": "registry.terraform.io/hashicorp/aws",
                "schema_version": 0,
                "values": {
                  "description": "Europe (Ireland)",
                  "endpoint": "ec2.eu-west-1.amazonaws.com",
                  "id": "eu-west-1",
                  "name": "eu-west-1",
                  "region": "eu-west-1"
                },
                "sensitive_values": {}
              }
            ],
            "address": "module.blueprint",
            "child_modules": [
              {
                "resources": [
                  {
                    "address": "module.blueprint.module.glue_catalog_database[\"raw_db\"].data.aws_caller_identity.current",
                    "mode": "data",
                    "type": "aws_caller_identity",
                    "name": "current",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "account_id": "899076912694",
                      "arn": "arn:aws:iam::899076912694:user/eniaws-sa-ictd-2102_pscoped_01",
                      "id": "899076912694",
                      "user_id": "AIDA5CVJI6Y3ARMQZ2JO3"
                    },
                    "sensitive_values": {}
                  },
                  {
                    "address": "module.blueprint.module.glue_catalog_database[\"raw_db\"].data.aws_iam_policy_document.custom_iam_policy_document[\"0\"]",
                    "mode": "data",
                    "type": "aws_iam_policy_document",
                    "name": "custom_iam_policy_document",
                    "index": "0",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "1680942515",
                      "json": "{\n  \"Version\": \"2012-10-17\",\n  \"Statement\": [\n    {\n      \"Sid\": \"GlueDatabaseRead\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"glue:GetTables\",\n        \"glue:GetDatabase\"\n      ],\n      \"Resource\": [\n        \"arn:aws:glue:eu-west-1:899076912694:table/raw_db/*\",\n        \"arn:aws:glue:eu-west-1:899076912694:database/raw_db\",\n        \"arn:aws:glue:eu-west-1:899076912694:catalog\"\n      ]\n    }\n  ]\n}",
                      "minified_json": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Sid\":\"GlueDatabaseRead\",\"Effect\":\"Allow\",\"Action\":[\"glue:GetTables\",\"glue:GetDatabase\"],\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/raw_db/*\",\"arn:aws:glue:eu-west-1:899076912694:database/raw_db\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"]}]}",
                      "override_json": null,
                      "override_policy_documents": null,
                      "policy_id": null,
                      "source_json": null,
                      "source_policy_documents": null,
                      "statement": [
                        {
                          "actions": [
                            "glue:GetDatabase",
                            "glue:GetTables"
                          ],
                          "condition": [],
                          "effect": "Allow",
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            "arn:aws:glue:eu-west-1:899076912694:catalog",
                            "arn:aws:glue:eu-west-1:899076912694:database/raw_db",
                            "arn:aws:glue:eu-west-1:899076912694:table/raw_db/*"
                          ],
                          "sid": "GlueDatabaseRead"
                        }
                      ],
                      "version": "2012-10-17"
                    },
                    "sensitive_values": {
                      "statement": [
                        {
                          "actions": [
                            false,
                            false
                          ],
                          "condition": [],
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            false,
                            false,
                            false
                          ]
                        }
                      ]
                    }
                  }
                ],
                "address": "module.blueprint.module.glue_catalog_database[\"raw_db\"]"
              },
              {
                "resources": [
                  {
                    "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].data.aws_caller_identity.current",
                    "mode": "data",
                    "type": "aws_caller_identity",
                    "name": "current",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "account_id": "899076912694",
                      "arn": "arn:aws:iam::899076912694:user/eniaws-sa-ictd-2102_pscoped_01",
                      "id": "899076912694",
                      "user_id": "AIDA5CVJI6Y3ARMQZ2JO3"
                    },
                    "sensitive_values": {}
                  },
                  {
                    "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].data.aws_iam_policy_document.assume_role",
                    "mode": "data",
                    "type": "aws_iam_policy_document",
                    "name": "assume_role",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "2681768870",
                      "json": "{\n  \"Version\": \"2012-10-17\",\n  \"Statement\": [\n    {\n      \"Effect\": \"Allow\",\n      \"Action\": \"sts:AssumeRole\",\n      \"Principal\": {\n        \"Service\": \"glue.amazonaws.com\"\n      }\n    }\n  ]\n}",
                      "minified_json": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Effect\":\"Allow\",\"Action\":\"sts:AssumeRole\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}]}",
                      "override_json": null,
                      "override_policy_documents": null,
                      "policy_id": null,
                      "source_json": null,
                      "source_policy_documents": null,
                      "statement": [
                        {
                          "actions": [
                            "sts:AssumeRole"
                          ],
                          "condition": [],
                          "effect": "Allow",
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [
                            {
                              "identifiers": [
                                "glue.amazonaws.com"
                              ],
                              "type": "Service"
                            }
                          ],
                          "resources": [],
                          "sid": ""
                        }
                      ],
                      "version": "2012-10-17"
                    },
                    "sensitive_values": {
                      "statement": [
                        {
                          "actions": [
                            false
                          ],
                          "condition": [],
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [
                            {
                              "identifiers": [
                                false
                              ]
                            }
                          ],
                          "resources": []
                        }
                      ]
                    }
                  },
                  {
                    "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].data.aws_iam_policy_document.combined",
                    "mode": "data",
                    "type": "aws_iam_policy_document",
                    "name": "combined",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "998259875",
                      "json": "{\n  \"Version\": \"2012-10-17\",\n  \"Statement\": [\n    {\n      \"Sid\": \"S3ListBucket\",\n      \"Effect\": \"Allow\",\n      \"Action\": \"s3:ListBucket\",\n      \"Resource\": \"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0\",\n      \"Condition\": {\n        \"StringLike\": {\n          \"s3:prefix\": [\n            \"raw//*\",\n            \"raw/\"\n          ]\n        }\n      }\n    },\n    {\n      \"Sid\": \"S3ReadObjects\",\n      \"Effect\": \"Allow\",\n      \"Action\": \"s3:GetObject\",\n      \"Resource\": \"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw//*\"\n    },\n    {\n      \"Sid\": \"GlueCatalogDbTableAccess\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"glue:UpdateTable\",\n        \"glue:UpdatePartition\",\n        \"glue:GetTables\",\n        \"glue:GetTable\",\n        \"glue:GetDatabases\",\n        \"glue:GetDatabase\",\n        \"glue:CreateTable\",\n        \"glue:CreatePartition\",\n        \"glue:BatchGetPartition\",\n        \"glue:BatchCreatePartition\"\n      ],\n      \"Resource\": [\n        \"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\n        \"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\n        \"arn:aws:glue:eu-west-1:899076912694:catalog\"\n      ]\n    },\n    {\n      \"Sid\": \"GlueCrawlerLogs\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"logs:PutLogEvents\",\n        \"logs:CreateLogStream\",\n        \"logs:CreateLogGroup\"\n      ],\n      \"Resource\": [\n        \"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\n        \"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"\n      ]\n    },\n    {\n      \"Sid\": \"GlueSecurityConfigurationAccess\",\n      \"Effect\": \"Allow\",\n      \"Action\": \"glue:GetSecurityConfiguration\",\n      \"Resource\": \"arn:aws:glue:eu-west-1:899076912694:security-configuration/eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp\"\n    }\n  ]\n}",
                      "minified_json": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Sid\":\"S3ListBucket\",\"Effect\":\"Allow\",\"Action\":\"s3:ListBucket\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0\",\"Condition\":{\"StringLike\":{\"s3:prefix\":[\"raw//*\",\"raw/\"]}}},{\"Sid\":\"S3ReadObjects\",\"Effect\":\"Allow\",\"Action\":\"s3:GetObject\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw//*\"},{\"Sid\":\"GlueCatalogDbTableAccess\",\"Effect\":\"Allow\",\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:GetTables\",\"glue:GetTable\",\"glue:GetDatabases\",\"glue:GetDatabase\",\"glue:CreateTable\",\"glue:CreatePartition\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"]},{\"Sid\":\"GlueCrawlerLogs\",\"Effect\":\"Allow\",\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"]},{\"Sid\":\"GlueSecurityConfigurationAccess\",\"Effect\":\"Allow\",\"Action\":\"glue:GetSecurityConfiguration\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:security-configuration/eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp\"}]}",
                      "override_json": null,
                      "override_policy_documents": null,
                      "policy_id": null,
                      "source_json": null,
                      "source_policy_documents": [
                        "{\n  \"Version\": \"2012-10-17\",\n  \"Statement\": [\n    {\n      \"Sid\": \"S3ListBucket\",\n      \"Effect\": \"Allow\",\n      \"Action\": \"s3:ListBucket\",\n      \"Resource\": \"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0\",\n      \"Condition\": {\n        \"StringLike\": {\n          \"s3:prefix\": [\n            \"raw//*\",\n            \"raw/\"\n          ]\n        }\n      }\n    },\n    {\n      \"Sid\": \"S3ReadObjects\",\n      \"Effect\": \"Allow\",\n      \"Action\": \"s3:GetObject\",\n      \"Resource\": \"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw//*\"\n    },\n    {\n      \"Sid\": \"GlueCatalogDbTableAccess\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"glue:UpdateTable\",\n        \"glue:UpdatePartition\",\n        \"glue:GetTables\",\n        \"glue:GetTable\",\n        \"glue:GetDatabases\",\n        \"glue:GetDatabase\",\n        \"glue:CreateTable\",\n        \"glue:CreatePartition\",\n        \"glue:BatchGetPartition\",\n        \"glue:BatchCreatePartition\"\n      ],\n      \"Resource\": [\n        \"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\n        \"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\n        \"arn:aws:glue:eu-west-1:899076912694:catalog\"\n      ]\n    },\n    {\n      \"Sid\": \"GlueCrawlerLogs\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"logs:PutLogEvents\",\n        \"logs:CreateLogStream\",\n        \"logs:CreateLogGroup\"\n      ],\n      \"Resource\": [\n        \"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\n        \"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"\n      ]\n    },\n    {\n      \"Sid\": \"GlueSecurityConfigurationAccess\",\n      \"Effect\": \"Allow\",\n      \"Action\": \"glue:GetSecurityConfiguration\",\n      \"Resource\": \"arn:aws:glue:eu-west-1:899076912694:security-configuration/eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp\"\n    }\n  ]\n}"
                      ],
                      "statement": null,
                      "version": "2012-10-17"
                    },
                    "sensitive_values": {
                      "source_policy_documents": [
                        false
                      ]
                    }
                  },
                  {
                    "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].data.aws_iam_policy_document.glue_crawler_policy",
                    "mode": "data",
                    "type": "aws_iam_policy_document",
                    "name": "glue_crawler_policy",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "998259875",
                      "json": "{\n  \"Version\": \"2012-10-17\",\n  \"Statement\": [\n    {\n      \"Sid\": \"S3ListBucket\",\n      \"Effect\": \"Allow\",\n      \"Action\": \"s3:ListBucket\",\n      \"Resource\": \"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0\",\n      \"Condition\": {\n        \"StringLike\": {\n          \"s3:prefix\": [\n            \"raw//*\",\n            \"raw/\"\n          ]\n        }\n      }\n    },\n    {\n      \"Sid\": \"S3ReadObjects\",\n      \"Effect\": \"Allow\",\n      \"Action\": \"s3:GetObject\",\n      \"Resource\": \"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw//*\"\n    },\n    {\n      \"Sid\": \"GlueCatalogDbTableAccess\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"glue:UpdateTable\",\n        \"glue:UpdatePartition\",\n        \"glue:GetTables\",\n        \"glue:GetTable\",\n        \"glue:GetDatabases\",\n        \"glue:GetDatabase\",\n        \"glue:CreateTable\",\n        \"glue:CreatePartition\",\n        \"glue:BatchGetPartition\",\n        \"glue:BatchCreatePartition\"\n      ],\n      \"Resource\": [\n        \"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\n        \"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\n        \"arn:aws:glue:eu-west-1:899076912694:catalog\"\n      ]\n    },\n    {\n      \"Sid\": \"GlueCrawlerLogs\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"logs:PutLogEvents\",\n        \"logs:CreateLogStream\",\n        \"logs:CreateLogGroup\"\n      ],\n      \"Resource\": [\n        \"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\n        \"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"\n      ]\n    },\n    {\n      \"Sid\": \"GlueSecurityConfigurationAccess\",\n      \"Effect\": \"Allow\",\n      \"Action\": \"glue:GetSecurityConfiguration\",\n      \"Resource\": \"arn:aws:glue:eu-west-1:899076912694:security-configuration/eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp\"\n    }\n  ]\n}",
                      "minified_json": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Sid\":\"S3ListBucket\",\"Effect\":\"Allow\",\"Action\":\"s3:ListBucket\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0\",\"Condition\":{\"StringLike\":{\"s3:prefix\":[\"raw//*\",\"raw/\"]}}},{\"Sid\":\"S3ReadObjects\",\"Effect\":\"Allow\",\"Action\":\"s3:GetObject\",\"Resource\":\"arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw//*\"},{\"Sid\":\"GlueCatalogDbTableAccess\",\"Effect\":\"Allow\",\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:GetTables\",\"glue:GetTable\",\"glue:GetDatabases\",\"glue:GetDatabase\",\"glue:CreateTable\",\"glue:CreatePartition\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Resource\":[\"arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*\",\"arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw\",\"arn:aws:glue:eu-west-1:899076912694:catalog\"]},{\"Sid\":\"GlueCrawlerLogs\",\"Effect\":\"Allow\",\"Action\":[\"logs:PutLogEvents\",\"logs:CreateLogStream\",\"logs:CreateLogGroup\"],\"Resource\":[\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*\",\"arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*\"]},{\"Sid\":\"GlueSecurityConfigurationAccess\",\"Effect\":\"Allow\",\"Action\":\"glue:GetSecurityConfiguration\",\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:security-configuration/eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp\"}]}",
                      "override_json": null,
                      "override_policy_documents": null,
                      "policy_id": null,
                      "source_json": null,
                      "source_policy_documents": null,
                      "statement": [
                        {
                          "actions": [
                            "s3:ListBucket"
                          ],
                          "condition": [
                            {
                              "test": "StringLike",
                              "values": [
                                "raw//*",
                                "raw/"
                              ],
                              "variable": "s3:prefix"
                            }
                          ],
                          "effect": "Allow",
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0"
                          ],
                          "sid": "S3ListBucket"
                        },
                        {
                          "actions": [
                            "s3:GetObject"
                          ],
                          "condition": [],
                          "effect": "Allow",
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-dpf-bp-l0/raw//*"
                          ],
                          "sid": "S3ReadObjects"
                        },
                        {
                          "actions": [
                            "glue:BatchCreatePartition",
                            "glue:BatchGetPartition",
                            "glue:CreatePartition",
                            "glue:CreateTable",
                            "glue:GetDatabase",
                            "glue:GetDatabases",
                            "glue:GetTable",
                            "glue:GetTables",
                            "glue:UpdatePartition",
                            "glue:UpdateTable"
                          ],
                          "condition": [],
                          "effect": "Allow",
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            "arn:aws:glue:eu-west-1:899076912694:catalog",
                            "arn:aws:glue:eu-west-1:899076912694:database/eniaws-glue-cat-euwe1-ictd-899076912694-raw",
                            "arn:aws:glue:eu-west-1:899076912694:table/eniaws-glue-cat-euwe1-ictd-899076912694-raw/*"
                          ],
                          "sid": "GlueCatalogDbTableAccess"
                        },
                        {
                          "actions": [
                            "logs:CreateLogGroup",
                            "logs:CreateLogStream",
                            "logs:PutLogEvents"
                          ],
                          "condition": [],
                          "effect": "Allow",
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            "arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*",
                            "arn:aws:logs:eu-west-1:899076912694:log-group:/aws-glue/crawlers*:log-stream:*"
                          ],
                          "sid": "GlueCrawlerLogs"
                        },
                        {
                          "actions": [
                            "glue:GetSecurityConfiguration"
                          ],
                          "condition": [],
                          "effect": "Allow",
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            "arn:aws:glue:eu-west-1:899076912694:security-configuration/eniaws-glue-sec-euwe1-ictd-899076912694-dpf-bp"
                          ],
                          "sid": "GlueSecurityConfigurationAccess"
                        }
                      ],
                      "version": "2012-10-17"
                    },
                    "sensitive_values": {
                      "statement": [
                        {
                          "actions": [
                            false
                          ],
                          "condition": [
                            {
                              "values": [
                                false,
                                false
                              ]
                            }
                          ],
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            false
                          ]
                        },
                        {
                          "actions": [
                            false
                          ],
                          "condition": [],
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            false
                          ]
                        },
                        {
                          "actions": [
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false
                          ],
                          "condition": [],
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            false,
                            false,
                            false
                          ]
                        },
                        {
                          "actions": [
                            false,
                            false,
                            false
                          ],
                          "condition": [],
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            false,
                            false
                          ]
                        },
                        {
                          "actions": [
                            false
                          ],
                          "condition": [],
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            false
                          ]
                        }
                      ]
                    }
                  }
                ],
                "address": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"]"
              },
              {
                "resources": [
                  {
                    "address": "module.blueprint.module.glue_job.data.aws_caller_identity.current",
                    "mode": "data",
                    "type": "aws_caller_identity",
                    "name": "current",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "account_id": "899076912694",
                      "arn": "arn:aws:iam::899076912694:user/eniaws-sa-ictd-2102_pscoped_01",
                      "id": "899076912694",
                      "user_id": "AIDA5CVJI6Y3ARMQZ2JO3"
                    },
                    "sensitive_values": {}
                  },
                  {
                    "address": "module.blueprint.module.glue_job.data.aws_iam_policy_document.assume_role",
                    "mode": "data",
                    "type": "aws_iam_policy_document",
                    "name": "assume_role",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "2681768870",
                      "json": "{\n  \"Version\": \"2012-10-17\",\n  \"Statement\": [\n    {\n      \"Effect\": \"Allow\",\n      \"Action\": \"sts:AssumeRole\",\n      \"Principal\": {\n        \"Service\": \"glue.amazonaws.com\"\n      }\n    }\n  ]\n}",
                      "minified_json": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Effect\":\"Allow\",\"Action\":\"sts:AssumeRole\",\"Principal\":{\"Service\":\"glue.amazonaws.com\"}}]}",
                      "override_json": null,
                      "override_policy_documents": null,
                      "policy_id": null,
                      "source_json": null,
                      "source_policy_documents": null,
                      "statement": [
                        {
                          "actions": [
                            "sts:AssumeRole"
                          ],
                          "condition": [],
                          "effect": "Allow",
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [
                            {
                              "identifiers": [
                                "glue.amazonaws.com"
                              ],
                              "type": "Service"
                            }
                          ],
                          "resources": [],
                          "sid": ""
                        }
                      ],
                      "version": "2012-10-17"
                    },
                    "sensitive_values": {
                      "statement": [
                        {
                          "actions": [
                            false
                          ],
                          "condition": [],
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [
                            {
                              "identifiers": [
                                false
                              ]
                            }
                          ],
                          "resources": []
                        }
                      ]
                    }
                  },
                  {
                    "address": "module.blueprint.module.glue_job.data.aws_iam_policy_document.custom_iam_policy_document[\"0\"]",
                    "mode": "data",
                    "type": "aws_iam_policy_document",
                    "name": "custom_iam_policy_document",
                    "index": "0",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "1645685932",
                      "json": "{\n  \"Version\": \"2012-10-17\",\n  \"Statement\": [\n    {\n      \"Sid\": \"AllowRestrictedGlueActions\",\n      \"Effect\": \"Allow\",\n      \"Action\": [\n        \"glue:UpdateTable\",\n        \"glue:UpdatePartition\",\n        \"glue:UpdateJob\",\n        \"glue:StartJobRun\",\n        \"glue:GetTable\",\n        \"glue:GetPartition\",\n        \"glue:GetJobRun\",\n        \"glue:GetJob\",\n        \"glue:GetDatabase\",\n        \"glue:BatchUpdatePartition\",\n        \"glue:BatchStopJobRun\",\n        \"glue:BatchGetPartition\",\n        \"glue:BatchCreatePartition\"\n      ],\n      \"Resource\": \"arn:aws:glue:eu-west-1:899076912694:*\"\n    }\n  ]\n}",
                      "minified_json": "{\"Version\":\"2012-10-17\",\"Statement\":[{\"Sid\":\"AllowRestrictedGlueActions\",\"Effect\":\"Allow\",\"Action\":[\"glue:UpdateTable\",\"glue:UpdatePartition\",\"glue:UpdateJob\",\"glue:StartJobRun\",\"glue:GetTable\",\"glue:GetPartition\",\"glue:GetJobRun\",\"glue:GetJob\",\"glue:GetDatabase\",\"glue:BatchUpdatePartition\",\"glue:BatchStopJobRun\",\"glue:BatchGetPartition\",\"glue:BatchCreatePartition\"],\"Resource\":\"arn:aws:glue:eu-west-1:899076912694:*\"}]}",
                      "override_json": null,
                      "override_policy_documents": null,
                      "policy_id": null,
                      "source_json": null,
                      "source_policy_documents": null,
                      "statement": [
                        {
                          "actions": [
                            "glue:BatchCreatePartition",
                            "glue:BatchGetPartition",
                            "glue:BatchStopJobRun",
                            "glue:BatchUpdatePartition",
                            "glue:GetDatabase",
                            "glue:GetJob",
                            "glue:GetJobRun",
                            "glue:GetPartition",
                            "glue:GetTable",
                            "glue:StartJobRun",
                            "glue:UpdateJob",
                            "glue:UpdatePartition",
                            "glue:UpdateTable"
                          ],
                          "condition": [],
                          "effect": "Allow",
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            "arn:aws:glue:eu-west-1:899076912694:*"
                          ],
                          "sid": "AllowRestrictedGlueActions"
                        }
                      ],
                      "version": "2012-10-17"
                    },
                    "sensitive_values": {
                      "statement": [
                        {
                          "actions": [
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false,
                            false
                          ],
                          "condition": [],
                          "not_actions": [],
                          "not_principals": [],
                          "not_resources": [],
                          "principals": [],
                          "resources": [
                            false
                          ]
                        }
                      ]
                    }
                  },
                  {
                    "address": "module.blueprint.module.glue_job.data.aws_partition.current",
                    "mode": "data",
                    "type": "aws_partition",
                    "name": "current",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "dns_suffix": "amazonaws.com",
                      "id": "aws",
                      "partition": "aws",
                      "reverse_dns_prefix": "com.amazonaws"
                    },
                    "sensitive_values": {}
                  }
                ],
                "address": "module.blueprint.module.glue_job"
              },
              {
                "resources": [
                  {
                    "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.combined_custom",
                    "mode": "data",
                    "type": "aws_iam_policy_document",
                    "name": "combined_custom",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "id": "1132004489",
                      "json": "{\n  \"Version\": \"2012-10-17\"\n}",
                      "minified_json": "{\"Version\":\"2012-10-17\"}",
                      "override_json": null,
                      "override_policy_documents": null,
                      "policy_id": null,
                      "source_json": null,
                      "source_policy_documents": null,
                      "statement": null,
                      "version": "2012-10-17"
                    },
                    "sensitive_values": {}
                  },
                  {
                    "address": "module.blueprint.module.s3_bucket_artifacts.data.aws_s3_bucket.bucket_s3_access_logs",
                    "mode": "data",
                    "type": "aws_s3_bucket",
                    "name": "bucket_s3_access_logs",
                    "provider_name": "registry.terraform.io/hashicorp/aws",
                    "schema_version": 0,
                    "values": {
                      "arn": "arn:aws:s3:::eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                      "bucket": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                      "bucket_domain_name": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs.s3.amazonaws.com",
                      "bucket_region": "eu-west-1",
                      "bucket_regional_domain_name": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs.s3.eu-west-1.amazonaws.com",
                      "hosted_zone_id": "Z1BKCTXD74EZPE",
                      "id": "eniaws-s3-euwe1-ictd-899076912694-s3-access-logs",
                      "region": "eu-west-1",
                      "website_domain": null,
                      "website_endpoint": null
                    },
                    "sensitive_values": {}
                  }
                ],
                "address": "module.blueprint.module.s3_bucket_artifacts"
              }
            ]
          }
        ]
      }
    }
  },
  "configuration": {
    "provider_config": {
      "aws": {
        "name": "aws",
        "full_name": "registry.terraform.io/hashicorp/aws",
        "version_constraint": "~> 6.8",
        "expressions": {
          "region": {
            "references": [
              "var.aws_region"
            ]
          }
        }
      }
    },
    "root_module": {
      "resources": [
        {
          "address": "data.aws_caller_identity.current",
          "mode": "data",
          "type": "aws_caller_identity",
          "name": "current",
          "provider_config_key": "aws",
          "schema_version": 0
        },
        {
          "address": "data.aws_region.current",
          "mode": "data",
          "type": "aws_region",
          "name": "current",
          "provider_config_key": "aws",
          "schema_version": 0
        }
      ],
      "module_calls": {
        "blueprint": {
          "source": "../../modules/blueprint",
          "expressions": {
            "custom_tags_glue": {
              "references": [
                "var.custom_tags_glue"
              ]
            },
            "deny_exception_principals": {
              "references": [
                "var.deny_exception_principals"
              ]
            },
            "department": {
              "references": [
                "var.department"
              ]
            },
            "env": {
              "references": [
                "var.env"
              ]
            },
            "glue_crawlers": {
              "references": [
                "var.glue_crawlers"
              ]
            },
            "glue_databases": {
              "references": [
                "var.glue_databases"
              ]
            },
            "glue_iam_policies": {
              "references": [
                "var.glue_iam_policies"
              ]
            },
            "glue_version": {
              "references": [
                "var.glue_version"
              ]
            },
            "number_of_workers": {
              "references": [
                "var.number_of_workers"
              ]
            },
            "s3_bucket_artifacts": {
              "references": [
                "var.s3_bucket_artifacts"
              ]
            },
            "scope": {
              "references": [
                "var.scope"
              ]
            },
            "worker_type": {
              "references": [
                "var.worker_type"
              ]
            }
          },
          "module": {
            "outputs": {
              "bucket_artifacts_name": {
                "expression": {
                  "references": [
                    "module.s3_bucket_artifacts.s3_bucket_id",
                    "module.s3_bucket_artifacts"
                  ]
                }
              },
              "glue_database_names": {
                "expression": {
                  "references": [
                    "module.glue_catalog_database"
                  ]
                }
              }
            },
            "resources": [
              {
                "address": "aws_glue_catalog_table.databases",
                "mode": "managed",
                "type": "aws_glue_catalog_table",
                "name": "databases",
                "provider_config_key": "aws",
                "expressions": {
                  "database_name": {
                    "references": [
                      "each.value.glue_database_key",
                      "each.value"
                    ]
                  },
                  "name": {
                    "references": [
                      "each.value.name",
                      "each.value"
                    ]
                  },
                  "parameters": {
                    "references": [
                      "each.value.parameters",
                      "each.value"
                    ]
                  },
                  "storage_descriptor": [
                    {
                      "input_format": {
                        "references": [
                          "each.value.storage.input_format",
                          "each.value.storage",
                          "each.value"
                        ]
                      },
                      "location": {
                        "references": [
                          "local.table_location",
                          "each.key"
                        ]
                      },
                      "output_format": {
                        "references": [
                          "each.value.storage.output_format",
                          "each.value.storage",
                          "each.value"
                        ]
                      },
                      "ser_de_info": [
                        {
                          "parameters": {
                            "references": [
                              "each.value.storage.serde_parameters",
                              "each.value.storage",
                              "each.value"
                            ]
                          },
                          "serialization_library": {
                            "references": [
                              "each.value.storage.serde_library",
                              "each.value.storage",
                              "each.value"
                            ]
                          }
                        }
                      ]
                    }
                  ],
                  "table_type": {
                    "references": [
                      "each.value.table_type",
                      "each.value"
                    ]
                  }
                },
                "schema_version": 0,
                "for_each_expression": {
                  "references": [
                    "local.glue_tables"
                  ]
                }
              },
              {
                "address": "data.aws_caller_identity.current",
                "mode": "data",
                "type": "aws_caller_identity",
                "name": "current",
                "provider_config_key": "aws",
                "schema_version": 0
              },
              {
                "address": "data.aws_region.current",
                "mode": "data",
                "type": "aws_region",
                "name": "current",
                "provider_config_key": "aws",
                "schema_version": 0
              }
            ],
            "module_calls": {
              "glue_catalog_database": {
                "source": "../../modules/glue/glue_catalog_database",
                "expressions": {
                  "aws_account_id": {
                    "references": [
                      "data.aws_caller_identity.current.account_id",
                      "data.aws_caller_identity.current"
                    ]
                  },
                  "aws_region": {
                    "references": [
                      "data.aws_region.current.region",
                      "data.aws_region.current"
                    ]
                  },
                  "custom_tags": {
                    "references": [
                      "each.value.custom_tags",
                      "each.value"
                    ]
                  },
                  "department": {
                    "references": [
                      "var.department"
                    ]
                  },
                  "description": {
                    "references": [
                      "each.value.description",
                      "each.value"
                    ]
                  },
                  "env": {
                    "references": [
                      "var.env"
                    ]
                  },
                  "iam_policies": {
                    "references": [
                      "each.value.iam_policies",
                      "each.value"
                    ]
                  },
                  "scope": {
                    "references": [
                      "each.value.scope",
                      "each.value"
                    ]
                  }
                },
                "for_each_expression": {
                  "references": [
                    "var.glue_databases"
                  ]
                },
                "module": {
                  "outputs": {
                    "aws_iam_policy": {
                      "expression": {
                        "references": [
                          "aws_iam_policy.iam_policy"
                        ]
                      },
                      "description": "The IAM policies created for the Glue Catalog Database (structured for tests)."
                    },
                    "glue_database_name": {
                      "expression": {
                        "references": [
                          "aws_glue_catalog_database.catalog.name",
                          "aws_glue_catalog_database.catalog"
                        ]
                      }
                    },
                    "glue_database_policies": {
                      "expression": {
                        "references": [
                          "aws_iam_policy.iam_policy"
                        ]
                      },
                      "description": "The IAM policies created for the Glue Catalog Database."
                    }
                  },
                  "resources": [
                    {
                      "address": "aws_glue_catalog_database.catalog",
                      "mode": "managed",
                      "type": "aws_glue_catalog_database",
                      "name": "catalog",
                      "provider_config_key": "aws",
                      "expressions": {
                        "description": {
                          "references": [
                            "var.description"
                          ]
                        },
                        "name": {
                          "references": [
                            "local.region_short_names",
                            "var.aws_region",
                            "var.department",
                            "var.env",
                            "var.aws_account_id",
                            "var.scope"
                          ]
                        },
                        "tags": {
                          "references": [
                            "var.custom_tags"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_iam_policy.iam_policy",
                      "mode": "managed",
                      "type": "aws_iam_policy",
                      "name": "iam_policy",
                      "provider_config_key": "aws",
                      "expressions": {
                        "name": {
                          "references": [
                            "each.key",
                            "var.scope"
                          ]
                        },
                        "policy": {
                          "references": [
                            "each.value.json",
                            "each.value"
                          ]
                        }
                      },
                      "schema_version": 0,
                      "for_each_expression": {
                        "references": [
                          "data.aws_iam_policy_document.custom_iam_policy_document"
                        ]
                      }
                    },
                    {
                      "address": "data.aws_caller_identity.current",
                      "mode": "data",
                      "type": "aws_caller_identity",
                      "name": "current",
                      "provider_config_key": "aws",
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.custom_iam_policy_document",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "custom_iam_policy_document",
                      "provider_config_key": "aws",
                      "schema_version": 0,
                      "for_each_expression": {
                        "references": [
                          "var.iam_policies"
                        ]
                      }
                    }
                  ],
                  "variables": {
                    "aws_account_id": {
                      "description": "The AWS account ID"
                    },
                    "aws_region": {
                      "description": "The AWS region"
                    },
                    "custom_tags": {
                      "description": "Tags specific for the application"
                    },
                    "department": {
                      "description": "The department name"
                    },
                    "description": {
                      "default": null,
                      "description": "Catalog Database description"
                    },
                    "env": {
                      "description": "The environment name"
                    },
                    "iam_policies": {
                      "default": [],
                      "description": "Custom IAM policies list for Glue catalog database"
                    },
                    "scope": {
                      "description": "The scope name"
                    }
                  }
                }
              },
              "glue_crawler": {
                "source": "../glue/glue_crawler",
                "expressions": {
                  "aws_account_id": {
                    "references": [
                      "data.aws_caller_identity.current.account_id",
                      "data.aws_caller_identity.current"
                    ]
                  },
                  "aws_region": {
                    "references": [
                      "data.aws_region.current.region",
                      "data.aws_region.current"
                    ]
                  },
                  "crawler_s3_target_path": {
                    "references": [
                      "each.value.crawler_s3_target_path",
                      "each.value"
                    ]
                  },
                  "custom_tags": {
                    "references": [
                      "each.value.custom_tags",
                      "each.value"
                    ]
                  },
                  "database_name": {
                    "references": [
                      "module.glue_catalog_database",
                      "each.value.database_key",
                      "each.value"
                    ]
                  },
                  "default_permissions_boundary": {
                    "references": [
                      "each.value.default_permissions_boundary",
                      "each.value"
                    ]
                  },
                  "department": {
                    "references": [
                      "var.department"
                    ]
                  },
                  "env": {
                    "references": [
                      "var.env"
                    ]
                  },
                  "iam_policies": {
                    "references": [
                      "each.value.iam_policies",
                      "each.value"
                    ]
                  },
                  "lineage_configuration": {
                    "references": [
                      "each.value.lineage_configuration",
                      "each.value"
                    ]
                  },
                  "schedule": {
                    "references": [
                      "each.value.schedule",
                      "each.value"
                    ]
                  },
                  "schema_change_policy": {
                    "references": [
                      "each.value.schema_change_policy",
                      "each.value"
                    ]
                  },
                  "scope": {
                    "references": [
                      "each.value.scope",
                      "each.value"
                    ]
                  },
                  "security_configuration_name": {
                    "references": [
                      "module.glue_job.security_configuration_name",
                      "module.glue_job"
                    ]
                  },
                  "table_prefix": {
                    "references": [
                      "each.value.table_prefix",
                      "each.value"
                    ]
                  }
                },
                "for_each_expression": {
                  "references": [
                    "var.glue_crawlers"
                  ]
                },
                "module": {
                  "outputs": {
                    "aws_glue_crawler": {
                      "expression": {
                        "references": [
                          "aws_glue_crawler.crawler"
                        ]
                      }
                    },
                    "glue_crawler_database_name": {
                      "expression": {
                        "references": [
                          "aws_glue_crawler.crawler.database_name",
                          "aws_glue_crawler.crawler"
                        ]
                      }
                    },
                    "glue_crawler_name": {
                      "expression": {
                        "references": [
                          "aws_glue_crawler.crawler.name",
                          "aws_glue_crawler.crawler"
                        ]
                      }
                    },
                    "glue_crawler_role_arn": {
                      "expression": {
                        "references": [
                          "aws_iam_role.role.arn",
                          "aws_iam_role.role"
                        ]
                      }
                    },
                    "glue_crawler_role_name": {
                      "expression": {
                        "references": [
                          "aws_iam_role.role.name",
                          "aws_iam_role.role"
                        ]
                      }
                    },
                    "glue_crawler_schedule": {
                      "expression": {
                        "references": [
                          "aws_glue_crawler.crawler.schedule",
                          "aws_glue_crawler.crawler"
                        ]
                      }
                    }
                  },
                  "resources": [
                    {
                      "address": "aws_glue_crawler.crawler",
                      "mode": "managed",
                      "type": "aws_glue_crawler",
                      "name": "crawler",
                      "provider_config_key": "aws",
                      "expressions": {
                        "database_name": {
                          "references": [
                            "var.database_name"
                          ]
                        },
                        "name": {
                          "references": [
                            "local.region_short_names",
                            "var.aws_region",
                            "var.department",
                            "var.env",
                            "var.aws_account_id",
                            "var.scope"
                          ]
                        },
                        "role": {
                          "references": [
                            "aws_iam_role.role.arn",
                            "aws_iam_role.role"
                          ]
                        },
                        "s3_target": [
                          {
                            "path": {
                              "references": [
                                "var.crawler_s3_target_path"
                              ]
                            }
                          }
                        ],
                        "schedule": {
                          "references": [
                            "var.schedule"
                          ]
                        },
                        "security_configuration": {
                          "references": [
                            "var.security_configuration_name"
                          ]
                        },
                        "table_prefix": {
                          "references": [
                            "var.table_prefix"
                          ]
                        },
                        "tags": {
                          "references": [
                            "var.custom_tags"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_iam_role.role",
                      "mode": "managed",
                      "type": "aws_iam_role",
                      "name": "role",
                      "provider_config_key": "aws",
                      "expressions": {
                        "assume_role_policy": {
                          "references": [
                            "data.aws_iam_policy_document.assume_role.json",
                            "data.aws_iam_policy_document.assume_role"
                          ]
                        },
                        "name": {
                          "references": [
                            "local.region_short_names",
                            "var.aws_region",
                            "var.department",
                            "var.env",
                            "var.aws_account_id",
                            "var.scope"
                          ]
                        },
                        "permissions_boundary": {
                          "references": [
                            "var.default_permissions_boundary"
                          ]
                        },
                        "tags": {
                          "references": [
                            "var.custom_tags"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_iam_role_policy.glue_crawler_permissions",
                      "mode": "managed",
                      "type": "aws_iam_role_policy",
                      "name": "glue_crawler_permissions",
                      "provider_config_key": "aws",
                      "expressions": {
                        "name": {
                          "constant_value": "glue_crawler_permissions"
                        },
                        "policy": {
                          "references": [
                            "data.aws_iam_policy_document.combined.json",
                            "data.aws_iam_policy_document.combined"
                          ]
                        },
                        "role": {
                          "references": [
                            "aws_iam_role.role.id",
                            "aws_iam_role.role"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_caller_identity.current",
                      "mode": "data",
                      "type": "aws_caller_identity",
                      "name": "current",
                      "provider_config_key": "aws",
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.assume_role",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "assume_role",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "sts:AssumeRole"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "constant_value": [
                                    "glue.amazonaws.com"
                                  ]
                                },
                                "type": {
                                  "constant_value": "Service"
                                }
                              }
                            ]
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.combined",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "combined",
                      "provider_config_key": "aws",
                      "expressions": {
                        "source_policy_documents": {
                          "references": [
                            "data.aws_iam_policy_document.glue_crawler_policy.json",
                            "data.aws_iam_policy_document.glue_crawler_policy",
                            "data.aws_iam_policy_document.custom_iam_policy_document"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.custom_iam_policy_document",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "custom_iam_policy_document",
                      "provider_config_key": "aws",
                      "schema_version": 0,
                      "for_each_expression": {
                        "references": [
                          "var.iam_policies"
                        ]
                      }
                    },
                    {
                      "address": "data.aws_iam_policy_document.glue_crawler_policy",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "glue_crawler_policy",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "s3:ListBucket"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "resources": {
                              "references": [
                                "local.bucket_arn"
                              ]
                            },
                            "sid": {
                              "constant_value": "S3ListBucket"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "s3:GetObject"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "resources": {
                              "references": [
                                "local.objects_arn"
                              ]
                            },
                            "sid": {
                              "constant_value": "S3ReadObjects"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "glue:GetDatabase",
                                "glue:GetDatabases",
                                "glue:GetTable",
                                "glue:GetTables",
                                "glue:CreateTable",
                                "glue:UpdateTable",
                                "glue:BatchCreatePartition",
                                "glue:BatchGetPartition",
                                "glue:CreatePartition",
                                "glue:UpdatePartition"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id",
                                "var.aws_region",
                                "var.aws_account_id",
                                "var.database_name",
                                "var.aws_region",
                                "var.aws_account_id",
                                "var.database_name"
                              ]
                            },
                            "sid": {
                              "constant_value": "GlueCatalogDbTableAccess"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "logs:CreateLogGroup",
                                "logs:CreateLogStream",
                                "logs:PutLogEvents"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id",
                                "var.aws_region",
                                "var.aws_account_id"
                              ]
                            },
                            "sid": {
                              "constant_value": "GlueCrawlerLogs"
                            }
                          }
                        ]
                      },
                      "schema_version": 0
                    }
                  ],
                  "variables": {
                    "aws_account_id": {
                      "description": "The AWS account ID"
                    },
                    "aws_region": {
                      "description": "The AWS region"
                    },
                    "crawler_s3_target_path": {
                      "description": "S3 path for crawler target"
                    },
                    "custom_tags": {
                      "description": "Tags specific for the application"
                    },
                    "database_name": {
                      "description": "Glue Catalog Database name to crawl"
                    },
                    "default_permissions_boundary": {
                      "default": null,
                      "description": "The ARN of the policy that is used to set the permissions boundary for the role."
                    },
                    "department": {
                      "description": "The department name"
                    },
                    "env": {
                      "description": "The environment name"
                    },
                    "iam_policies": {
                      "default": [],
                      "description": "Custom IAM policies list for Glue crawler"
                    },
                    "lineage_configuration": {
                      "default": null,
                      "description": "Lineage configuration"
                    },
                    "schedule": {
                      "default": null,
                      "description": "Cron expression for crawler schedule"
                    },
                    "schema_change_policy": {
                      "default": null,
                      "description": "Schema change policy settings"
                    },
                    "scope": {
                      "description": "The scope name"
                    },
                    "security_configuration_name": {
                      "default": null,
                      "description": "Glue Security Configuration name to associate to the crawler"
                    },
                    "table_prefix": {
                      "default": null,
                      "description": "Optional table prefix"
                    }
                  }
                }
              },
              "glue_job": {
                "source": "../glue",
                "expressions": {
                  "aws_account_id": {
                    "references": [
                      "data.aws_caller_identity.current.account_id",
                      "data.aws_caller_identity.current"
                    ]
                  },
                  "aws_region": {
                    "references": [
                      "data.aws_region.current.region",
                      "data.aws_region.current"
                    ]
                  },
                  "custom_tags": {
                    "references": [
                      "var.custom_tags_glue"
                    ]
                  },
                  "default_permissions_boundary": {
                    "references": [
                      "data.aws_caller_identity.current.account_id",
                      "data.aws_caller_identity.current"
                    ]
                  },
                  "deny_exception_principals": {
                    "references": [
                      "var.deny_exception_principals"
                    ]
                  },
                  "department": {
                    "references": [
                      "var.department"
                    ]
                  },
                  "env": {
                    "references": [
                      "var.env"
                    ]
                  },
                  "glue_version": {
                    "references": [
                      "var.glue_version"
                    ]
                  },
                  "iam_policies": {
                    "references": [
                      "var.glue_iam_policies"
                    ]
                  },
                  "job_type": {
                    "constant_value": "glueetl"
                  },
                  "number_of_workers": {
                    "references": [
                      "var.number_of_workers"
                    ]
                  },
                  "scope": {
                    "references": [
                      "var.scope"
                    ]
                  },
                  "script_bucket_name": {
                    "references": [
                      "module.s3_bucket_artifacts.s3_bucket_id",
                      "module.s3_bucket_artifacts"
                    ]
                  },
                  "script_s3_key": {
                    "constant_value": "glue_jobs/src/job_main.py"
                  },
                  "worker_type": {
                    "references": [
                      "var.worker_type"
                    ]
                  }
                },
                "module": {
                  "outputs": {
                    "aws_glue_job": {
                      "expression": {
                        "references": [
                          "aws_glue_job.job"
                        ]
                      },
                      "description": "The Glue Job resources created."
                    },
                    "aws_iam_role_policy": {
                      "expression": {
                        "references": [
                          "aws_iam_role_policy.glue_job_permissions"
                        ]
                      },
                      "description": "The IAM Role Policy resources created."
                    },
                    "aws_s3_object": {
                      "expression": {
                        "references": [
                          "aws_s3_object.glue_etl_script"
                        ]
                      },
                      "description": "The S3 object resources created."
                    },
                    "glue_job_command": {
                      "expression": {
                        "references": [
                          "aws_glue_job.job.command",
                          "aws_glue_job.job"
                        ]
                      },
                      "description": "The command configuration of the Glue job."
                    },
                    "glue_job_default_arguments": {
                      "expression": {
                        "references": [
                          "aws_glue_job.job.default_arguments",
                          "aws_glue_job.job"
                        ]
                      },
                      "description": "The default arguments of the Glue job."
                    },
                    "glue_job_max_retries": {
                      "expression": {
                        "references": [
                          "aws_glue_job.job.max_retries",
                          "aws_glue_job.job"
                        ]
                      },
                      "description": "The max retries of the Glue job."
                    },
                    "glue_job_name": {
                      "expression": {
                        "references": [
                          "aws_glue_job.job.name",
                          "aws_glue_job.job"
                        ]
                      },
                      "description": "The name of the Glue job."
                    },
                    "glue_job_role_arn": {
                      "expression": {
                        "references": [
                          "aws_iam_role.role.arn",
                          "aws_iam_role.role"
                        ]
                      },
                      "description": "The ARN of the IAM role used by the Glue job."
                    },
                    "glue_job_role_assume_role_policy": {
                      "expression": {
                        "references": [
                          "aws_iam_role.role.assume_role_policy",
                          "aws_iam_role.role"
                        ]
                      },
                      "description": "The assume role policy of the IAM role."
                    },
                    "glue_job_role_name": {
                      "expression": {
                        "references": [
                          "aws_iam_role.role.name",
                          "aws_iam_role.role"
                        ]
                      },
                      "description": "The name of the IAM role used by the Glue job."
                    },
                    "glue_job_timeout": {
                      "expression": {
                        "references": [
                          "aws_glue_job.job.timeout",
                          "aws_glue_job.job"
                        ]
                      },
                      "description": "The timeout of the Glue job."
                    },
                    "glue_resource_policy_json": {
                      "expression": {
                        "references": [
                          "data.aws_iam_policy_document.glue_job_combined_policy.json",
                          "data.aws_iam_policy_document.glue_job_combined_policy"
                        ]
                      },
                      "description": "The JSON of the Glue Resource Policy. Use this to manually update the policy if Terraform fails."
                    },
                    "security_configuration_name": {
                      "expression": {
                        "references": [
                          "aws_glue_security_configuration.this.name",
                          "aws_glue_security_configuration.this"
                        ]
                      },
                      "description": "The name of the Glue Security Configuration."
                    }
                  },
                  "resources": [
                    {
                      "address": "aws_glue_job.job",
                      "mode": "managed",
                      "type": "aws_glue_job",
                      "name": "job",
                      "provider_config_key": "aws",
                      "expressions": {
                        "command": [
                          {
                            "name": {
                              "references": [
                                "var.job_type"
                              ]
                            },
                            "python_version": {
                              "references": [
                                "var.python_version"
                              ]
                            },
                            "script_location": {
                              "references": [
                                "var.script_bucket_name",
                                "var.script_s3_key"
                              ]
                            }
                          }
                        ],
                        "default_arguments": {
                          "references": [
                            "var.job_type",
                            "var.default_arguments"
                          ]
                        },
                        "description": {
                          "references": [
                            "var.job_description"
                          ]
                        },
                        "execution_class": {
                          "references": [
                            "var.execution_class"
                          ]
                        },
                        "execution_property": [
                          {
                            "max_concurrent_runs": {
                              "references": [
                                "var.max_concurrent_runs"
                              ]
                            }
                          }
                        ],
                        "glue_version": {
                          "references": [
                            "var.job_type",
                            "var.glue_version"
                          ]
                        },
                        "max_capacity": {
                          "references": [
                            "var.job_type",
                            "var.max_capacity"
                          ]
                        },
                        "max_retries": {
                          "references": [
                            "var.max_retries"
                          ]
                        },
                        "name": {
                          "references": [
                            "local.region_short_names",
                            "var.aws_region",
                            "var.department",
                            "var.env",
                            "var.aws_account_id",
                            "var.scope"
                          ]
                        },
                        "notification_property": [
                          {
                            "notify_delay_after": {
                              "references": [
                                "var.notification_delay"
                              ]
                            }
                          }
                        ],
                        "number_of_workers": {
                          "references": [
                            "var.job_type",
                            "var.number_of_workers"
                          ]
                        },
                        "role_arn": {
                          "references": [
                            "aws_iam_role.role.arn",
                            "aws_iam_role.role"
                          ]
                        },
                        "security_configuration": {
                          "references": [
                            "aws_glue_security_configuration.this.name",
                            "aws_glue_security_configuration.this"
                          ]
                        },
                        "tags": {
                          "references": [
                            "local.tags"
                          ]
                        },
                        "timeout": {
                          "references": [
                            "var.timeout"
                          ]
                        },
                        "worker_type": {
                          "references": [
                            "var.job_type",
                            "var.worker_type"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_glue_resource_policy.this",
                      "mode": "managed",
                      "type": "aws_glue_resource_policy",
                      "name": "this",
                      "provider_config_key": "aws",
                      "expressions": {
                        "enable_hybrid": {
                          "constant_value": "TRUE"
                        },
                        "policy": {
                          "references": [
                            "data.aws_iam_policy_document.glue_resource_policy_doc.json",
                            "data.aws_iam_policy_document.glue_resource_policy_doc"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_glue_security_configuration.this",
                      "mode": "managed",
                      "type": "aws_glue_security_configuration",
                      "name": "this",
                      "provider_config_key": "aws",
                      "expressions": {
                        "encryption_configuration": [
                          {
                            "cloudwatch_encryption": [
                              {
                                "cloudwatch_encryption_mode": {
                                  "constant_value": "SSE-KMS"
                                },
                                "kms_key_arn": {
                                  "references": [
                                    "var.aws_region",
                                    "var.aws_account_id"
                                  ]
                                }
                              }
                            ],
                            "job_bookmarks_encryption": [
                              {
                                "job_bookmarks_encryption_mode": {
                                  "constant_value": "CSE-KMS"
                                },
                                "kms_key_arn": {
                                  "references": [
                                    "var.aws_region",
                                    "var.aws_account_id"
                                  ]
                                }
                              }
                            ],
                            "s3_encryption": [
                              {
                                "s3_encryption_mode": {
                                  "constant_value": "SSE-S3"
                                }
                              }
                            ]
                          }
                        ],
                        "name": {
                          "references": [
                            "local.region_short_names",
                            "var.aws_region",
                            "var.department",
                            "var.env",
                            "var.aws_account_id",
                            "var.scope"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_iam_role.role",
                      "mode": "managed",
                      "type": "aws_iam_role",
                      "name": "role",
                      "provider_config_key": "aws",
                      "expressions": {
                        "assume_role_policy": {
                          "references": [
                            "data.aws_iam_policy_document.assume_role.json",
                            "data.aws_iam_policy_document.assume_role"
                          ]
                        },
                        "name": {
                          "references": [
                            "local.region_short_names",
                            "var.aws_region",
                            "var.department",
                            "var.env",
                            "var.aws_account_id",
                            "var.scope"
                          ]
                        },
                        "permissions_boundary": {
                          "references": [
                            "var.default_permissions_boundary"
                          ]
                        },
                        "tags": {
                          "references": [
                            "var.custom_tags"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_iam_role_policy.glue_job_permissions",
                      "mode": "managed",
                      "type": "aws_iam_role_policy",
                      "name": "glue_job_permissions",
                      "provider_config_key": "aws",
                      "expressions": {
                        "name": {
                          "constant_value": "glue_job_permissions"
                        },
                        "policy": {
                          "references": [
                            "data.aws_iam_policy_document.glue_job_combined_policy.json",
                            "data.aws_iam_policy_document.glue_job_combined_policy"
                          ]
                        },
                        "role": {
                          "references": [
                            "aws_iam_role.role.id",
                            "aws_iam_role.role"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_s3_object.glue_etl_script",
                      "mode": "managed",
                      "type": "aws_s3_object",
                      "name": "glue_etl_script",
                      "provider_config_key": "aws",
                      "expressions": {
                        "bucket": {
                          "references": [
                            "var.script_bucket_name"
                          ]
                        },
                        "etag": {
                          "references": [
                            "var.local_script_path"
                          ]
                        },
                        "key": {
                          "references": [
                            "var.script_s3_key"
                          ]
                        },
                        "source": {
                          "references": [
                            "var.local_script_path"
                          ]
                        }
                      },
                      "schema_version": 0,
                      "count_expression": {
                        "references": [
                          "var.local_script_path"
                        ]
                      }
                    },
                    {
                      "address": "data.aws_caller_identity.current",
                      "mode": "data",
                      "type": "aws_caller_identity",
                      "name": "current",
                      "provider_config_key": "aws",
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.assume_role",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "assume_role",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "sts:AssumeRole"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "constant_value": [
                                    "glue.amazonaws.com"
                                  ]
                                },
                                "type": {
                                  "constant_value": "Service"
                                }
                              }
                            ]
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.custom_iam_policy_document",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "custom_iam_policy_document",
                      "provider_config_key": "aws",
                      "schema_version": 0,
                      "for_each_expression": {
                        "references": [
                          "var.iam_policies"
                        ]
                      }
                    },
                    {
                      "address": "data.aws_iam_policy_document.glue_job_combined_policy",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "glue_job_combined_policy",
                      "provider_config_key": "aws",
                      "expressions": {
                        "source_policy_documents": {
                          "references": [
                            "data.aws_iam_policy_document.glue_job_policy.json",
                            "data.aws_iam_policy_document.glue_job_policy",
                            "data.aws_iam_policy_document.custom_iam_policy_document"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.glue_job_policy",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "glue_job_policy",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "s3:GetObject",
                                "s3:PutObject",
                                "s3:DeleteObject",
                                "s3:ListBucket",
                                "s3:GetBucketLocation"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "resources": {
                              "references": [
                                "local.s3_resources"
                              ]
                            },
                            "sid": {
                              "constant_value": "S3Access"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "logs:CreateLogGroup",
                                "logs:CreateLogStream",
                                "logs:PutLogEvents",
                                "logs:DescribeLogGroups"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "resources": {
                              "constant_value": [
                                "arn:aws:logs:*:*:log-group:/aws-glue/*",
                                "arn:aws:logs:*:*:log-group:/aws-glue/*:*"
                              ]
                            },
                            "sid": {
                              "constant_value": "LogsAccess"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "cloudwatch:PutMetricData"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "resources": {
                              "constant_value": [
                                "*"
                              ]
                            },
                            "sid": {
                              "constant_value": "CloudWatchMetrics"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "glue:GetJob",
                                "glue:GetJobRun",
                                "glue:StartJobRun",
                                "glue:UpdateJob",
                                "glue:GetTable",
                                "glue:GetDatabase",
                                "glue:GetPartition",
                                "glue:BatchGetPartition",
                                "glue:UpdateTable",
                                "glue:UpdatePartition",
                                "glue:BatchCreatePartition",
                                "glue:BatchUpdatePartition",
                                "glue:BatchStopJobRun"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id"
                              ]
                            },
                            "sid": {
                              "constant_value": "GlueAccess"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "ec2:CreateNetworkInterface",
                                "ec2:DeleteNetworkInterface",
                                "ec2:AttachNetworkInterface",
                                "ec2:DetachNetworkInterface"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id",
                                "var.aws_region",
                                "var.aws_account_id",
                                "var.subnet_id",
                                "var.security_group_ids",
                                "var.aws_region",
                                "var.aws_account_id"
                              ]
                            },
                            "sid": {
                              "constant_value": "EC2Modify"
                            }
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.glue_resource_policy_doc",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "glue_resource_policy_doc",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "glue:*"
                              ]
                            },
                            "condition": [
                              {
                                "test": {
                                  "constant_value": "StringEquals"
                                },
                                "values": {
                                  "constant_value": [
                                    "638883080465"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:VpceAccount"
                                }
                              }
                            ],
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "constant_value": [
                                    "*"
                                  ]
                                },
                                "type": {
                                  "constant_value": "*"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id"
                              ]
                            },
                            "sid": {
                              "constant_value": "AllowActionsFromInsideVPC"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "glue:Get*",
                                "glue:List*",
                                "glue:BatchGet*"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "references": [
                                    "var.aws_account_id"
                                  ]
                                },
                                "type": {
                                  "constant_value": "AWS"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id"
                              ]
                            },
                            "sid": {
                              "constant_value": "AllowPrisma"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "glue:Get*",
                                "glue:List*",
                                "glue:BatchGet*"
                              ]
                            },
                            "condition": [
                              {
                                "test": {
                                  "constant_value": "StringEquals"
                                },
                                "values": {
                                  "constant_value": [
                                    "vpc-0fbd9e814ef60d4ac"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:SourceVpc"
                                }
                              },
                              {
                                "test": {
                                  "constant_value": "IpAddress"
                                },
                                "values": {
                                  "constant_value": [
                                    "10.68.98.160/27",
                                    "10.68.98.128/27"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:VpcSourceIp"
                                }
                              }
                            ],
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "constant_value": [
                                    "*"
                                  ]
                                },
                                "type": {
                                  "constant_value": "*"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id"
                              ]
                            },
                            "sid": {
                              "constant_value": "AllowPublicThroughF5"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "glue:*"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "references": [
                                    "local.aft_principals",
                                    "local.aft_principals",
                                    "var.aws_account_id"
                                  ]
                                },
                                "type": {
                                  "constant_value": "AWS"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id"
                              ]
                            },
                            "sid": {
                              "constant_value": "AllowAFTExecution"
                            }
                          },
                          {
                            "condition": [
                              {
                                "test": {
                                  "constant_value": "StringNotEquals"
                                },
                                "values": {
                                  "constant_value": [
                                    "638883080465"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:VpceAccount"
                                }
                              },
                              {
                                "test": {
                                  "constant_value": "NotIpAddress"
                                },
                                "values": {
                                  "constant_value": [
                                    "10.68.98.160/27",
                                    "10.68.98.128/27"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:VpcSourceIp"
                                }
                              },
                              {
                                "test": {
                                  "constant_value": "StringNotEquals"
                                },
                                "values": {
                                  "references": [
                                    "var.network_exposure",
                                    "var.aws_account_id",
                                    "var.aws_account_id",
                                    "var.deny_exception_principals",
                                    "local.aft_principals",
                                    "data.aws_caller_identity.current.arn",
                                    "data.aws_caller_identity.current",
                                    "var.aws_account_id",
                                    "aws_iam_role.role.arn",
                                    "aws_iam_role.role"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:PrincipalArn"
                                }
                              },
                              {
                                "test": {
                                  "constant_value": "BoolIfExists"
                                },
                                "values": {
                                  "constant_value": [
                                    "false"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:PrincipalIsAWSService"
                                }
                              }
                            ],
                            "effect": {
                              "constant_value": "Deny"
                            },
                            "not_actions": {
                              "constant_value": [
                                "glue:PutResourcePolicy",
                                "glue:GetResourcePolicy",
                                "glue:DeleteResourcePolicy",
                                "glue:Get*",
                                "glue:List*",
                                "glue:BatchGet*"
                              ]
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "constant_value": [
                                    "*"
                                  ]
                                },
                                "type": {
                                  "constant_value": "AWS"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id"
                              ]
                            },
                            "sid": {
                              "constant_value": "DenyNotPrincipals"
                            }
                          },
                          {
                            "actions": {
                              "constant_value": [
                                "glue:*"
                              ]
                            },
                            "condition": [
                              {
                                "test": {
                                  "constant_value": "Bool"
                                },
                                "values": {
                                  "constant_value": [
                                    "false"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:SecureTransport"
                                }
                              }
                            ],
                            "effect": {
                              "constant_value": "Deny"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "constant_value": [
                                    "*"
                                  ]
                                },
                                "type": {
                                  "constant_value": "*"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "var.aws_region",
                                "var.aws_account_id"
                              ]
                            },
                            "sid": {
                              "constant_value": "DenyNonHTTPS"
                            }
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_partition.current",
                      "mode": "data",
                      "type": "aws_partition",
                      "name": "current",
                      "provider_config_key": "aws",
                      "schema_version": 0
                    }
                  ],
                  "variables": {
                    "availability_zone": {
                      "default": "eu-west-1a",
                      "description": "Availability Zone for Glue connection"
                    },
                    "aws_account_id": {
                      "description": "The AWS account ID"
                    },
                    "aws_region": {
                      "description": "The AWS region"
                    },
                    "connection_type": {
                      "default": "NETWORK",
                      "description": "Glue connection type"
                    },
                    "custom_tags": {
                      "description": "Tags specific for the application"
                    },
                    "default_arguments": {
                      "default": {},
                      "description": "Additional default arguments for Glue job"
                    },
                    "default_permissions_boundary": {
                      "default": null,
                      "description": "The permissions boundary to apply to the IAM role"
                    },
                    "deny_exception_principals": {
                      "default": [],
                      "description": "List of AWS principals: they will not be under deny all actions if traffic source is not vpc"
                    },
                    "department": {
                      "description": "The department name"
                    },
                    "enable_glue_resource_policy": {
                      "default": true,
                      "description": "Whether to create the Glue Resource Policy"
                    },
                    "env": {
                      "description": "The environment name"
                    },
                    "execution_class": {
                      "default": "STANDARD",
                      "description": "Execution class"
                    },
                    "extra_s3_bucket_arns": {
                      "default": [],
                      "description": "List of extra S3 bucket ARNs to allow access to (e.g. arn:aws:s3:::my-bucket or arn:aws:s3:::my-bucket/*)"
                    },
                    "glue_version": {
                      "default": "5.0",
                      "description": "Glue version"
                    },
                    "iam_policies": {
                      "default": [],
                      "description": "Custom IAM policies list for Glue module"
                    },
                    "job_description": {
                      "default": "Glue ETL job",
                      "description": "Job description"
                    },
                    "job_type": {
                      "default": "glueetl",
                      "description": "Type of the job (glueetl or pythonshell)"
                    },
                    "lake_formation_configuration": {
                      "default": null,
                      "description": "Lake Formation configuration"
                    },
                    "lineage_configuration": {
                      "default": null,
                      "description": "Lineage configuration"
                    },
                    "local_script_path": {
                      "default": null,
                      "description": "Local path to ETL script source file"
                    },
                    "max_capacity": {
                      "default": 0.0625,
                      "description": "Max capacity for Python Shell jobs (0.0625 or 1)"
                    },
                    "max_concurrent_runs": {
                      "default": 1,
                      "description": "Max concurrent runs"
                    },
                    "max_retries": {
                      "default": 1,
                      "description": "Max retries"
                    },
                    "network_exposure": {
                      "default": "private",
                      "description": "Network exposure of Glue APIs (private/public) for policy conditions"
                    },
                    "notification_delay": {
                      "default": 3,
                      "description": "Delay in minutes for job notifications"
                    },
                    "number_of_workers": {
                      "default": 2,
                      "description": "Number of workers"
                    },
                    "policies": {
                      "default": [],
                      "description": "List of policies be added to the glue policy"
                    },
                    "python_version": {
                      "default": "3",
                      "description": "Python version for the job"
                    },
                    "schedule": {
                      "default": null,
                      "description": "Cron expression for crawler schedule"
                    },
                    "schema_change_policy": {
                      "default": null,
                      "description": "Schema change policy settings"
                    },
                    "scope": {
                      "description": "The scope name"
                    },
                    "script_bucket_name": {
                      "description": "S3 bucket name for ETL script"
                    },
                    "script_s3_key": {
                      "description": "S3 key (path) for ETL script"
                    },
                    "security_group_ids": {
                      "default": [
                        "sg-09096e91dd18fa7d4",
                        "sg-0aa6fd5972038141a",
                        "sg-0cb505f744b1c74eb",
                        "sg-032c47f80254c35c7"
                      ],
                      "description": "List of security group IDs for Glue connection"
                    },
                    "subnet_id": {
                      "default": "subnet-0a8409260cbaf999f",
                      "description": "List of subnet IDs for Glue VPC integration"
                    },
                    "table_prefix": {
                      "default": null,
                      "description": "Optional table prefix"
                    },
                    "timeout": {
                      "default": 2880,
                      "description": "Timeout (minutes)"
                    },
                    "vpc_id": {
                      "default": "vpc-0fbd9e814ef60d4ac",
                      "description": "Id of the vpc containing vpc endpoint"
                    },
                    "worker_type": {
                      "default": "G.1X",
                      "description": "Worker type"
                    }
                  }
                }
              },
              "s3_bucket_artifacts": {
                "source": "gitlab-dgt.eni.com/infra/s3/buildingblock",
                "expressions": {
                  "aws_account_id": {
                    "references": [
                      "data.aws_caller_identity.current.account_id",
                      "data.aws_caller_identity.current"
                    ]
                  },
                  "aws_region": {
                    "references": [
                      "data.aws_region.current.region",
                      "data.aws_region.current"
                    ]
                  },
                  "bucket_s3_access_logs_name": {
                    "references": [
                      "var.s3_bucket_artifacts.bucket_s3_access_logs_name",
                      "var.s3_bucket_artifacts"
                    ]
                  },
                  "custom_tags": {
                    "references": [
                      "var.s3_bucket_artifacts.custom_tags",
                      "var.s3_bucket_artifacts"
                    ]
                  },
                  "deny_exception_principals": {
                    "references": [
                      "var.s3_bucket_artifacts.deny_exception_principals",
                      "var.s3_bucket_artifacts"
                    ]
                  },
                  "department": {
                    "references": [
                      "var.department"
                    ]
                  },
                  "env": {
                    "references": [
                      "var.env"
                    ]
                  },
                  "iam_policies": {
                    "references": [
                      "var.s3_bucket_artifacts.iam_policies",
                      "var.s3_bucket_artifacts"
                    ]
                  },
                  "scope": {
                    "references": [
                      "var.scope"
                    ]
                  }
                },
                "module": {
                  "outputs": {
                    "iam_policy_arn": {
                      "expression": {
                        "references": [
                          "aws_iam_policy.iam_policy"
                        ]
                      }
                    },
                    "s3_arn": {
                      "expression": {
                        "references": [
                          "aws_s3_bucket.s3_bucket.arn",
                          "aws_s3_bucket.s3_bucket"
                        ]
                      }
                    },
                    "s3_bucket_id": {
                      "expression": {
                        "references": [
                          "aws_s3_bucket.s3_bucket.id",
                          "aws_s3_bucket.s3_bucket"
                        ]
                      }
                    }
                  },
                  "resources": [
                    {
                      "address": "aws_iam_policy.iam_policy",
                      "mode": "managed",
                      "type": "aws_iam_policy",
                      "name": "iam_policy",
                      "provider_config_key": "aws",
                      "expressions": {
                        "name": {
                          "references": [
                            "each.key",
                            "var.scope"
                          ]
                        },
                        "policy": {
                          "references": [
                            "each.value.json",
                            "each.value"
                          ]
                        }
                      },
                      "schema_version": 0,
                      "for_each_expression": {
                        "references": [
                          "data.aws_iam_policy_document.custom_iam_policy_document"
                        ]
                      }
                    },
                    {
                      "address": "aws_s3_bucket.s3_bucket",
                      "mode": "managed",
                      "type": "aws_s3_bucket",
                      "name": "s3_bucket",
                      "provider_config_key": "aws",
                      "expressions": {
                        "bucket": {
                          "references": [
                            "local.modified_region",
                            "var.department",
                            "var.env",
                            "var.aws_account_id",
                            "var.scope"
                          ]
                        },
                        "force_destroy": {
                          "constant_value": true
                        },
                        "tags": {
                          "references": [
                            "local.bb_tags",
                            "local.off_custom_tags"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_s3_bucket_lifecycle_configuration.bucket_lifecycle_configuration",
                      "mode": "managed",
                      "type": "aws_s3_bucket_lifecycle_configuration",
                      "name": "bucket_lifecycle_configuration",
                      "provider_config_key": "aws",
                      "expressions": {
                        "bucket": {
                          "references": [
                            "aws_s3_bucket.s3_bucket.id",
                            "aws_s3_bucket.s3_bucket"
                          ]
                        },
                        "rule": [
                          {
                            "filter": [
                              {}
                            ],
                            "id": {
                              "constant_value": "rule"
                            },
                            "noncurrent_version_expiration": [
                              {
                                "newer_noncurrent_versions": {
                                  "references": [
                                    "var.operational_backup.noncurrent_version_expiration.newer_noncurrent_versions",
                                    "var.operational_backup.noncurrent_version_expiration",
                                    "var.operational_backup"
                                  ]
                                },
                                "noncurrent_days": {
                                  "references": [
                                    "var.operational_backup.noncurrent_version_expiration.noncurrent_days",
                                    "var.operational_backup.noncurrent_version_expiration",
                                    "var.operational_backup"
                                  ]
                                }
                              }
                            ],
                            "noncurrent_version_transition": [
                              {
                                "newer_noncurrent_versions": {
                                  "references": [
                                    "var.operational_backup.noncurrent_version_transition.newer_noncurrent_versions",
                                    "var.operational_backup.noncurrent_version_transition",
                                    "var.operational_backup"
                                  ]
                                },
                                "noncurrent_days": {
                                  "references": [
                                    "var.operational_backup.noncurrent_version_transition.noncurrent_days",
                                    "var.operational_backup.noncurrent_version_transition",
                                    "var.operational_backup"
                                  ]
                                },
                                "storage_class": {
                                  "constant_value": "GLACIER"
                                }
                              }
                            ],
                            "status": {
                              "constant_value": "Enabled"
                            }
                          }
                        ]
                      },
                      "schema_version": 1,
                      "count_expression": {
                        "references": [
                          "var.operational_backup"
                        ]
                      },
                      "depends_on": [
                        "aws_s3_bucket_versioning.bucket_versioning"
                      ]
                    },
                    {
                      "address": "aws_s3_bucket_logging.example",
                      "mode": "managed",
                      "type": "aws_s3_bucket_logging",
                      "name": "example",
                      "provider_config_key": "aws",
                      "expressions": {
                        "bucket": {
                          "references": [
                            "aws_s3_bucket.s3_bucket.id",
                            "aws_s3_bucket.s3_bucket"
                          ]
                        },
                        "target_bucket": {
                          "references": [
                            "data.aws_s3_bucket.bucket_s3_access_logs.id",
                            "data.aws_s3_bucket.bucket_s3_access_logs"
                          ]
                        },
                        "target_object_key_format": [
                          {
                            "partitioned_prefix": [
                              {
                                "partition_date_source": {
                                  "constant_value": "EventTime"
                                }
                              }
                            ]
                          }
                        ],
                        "target_prefix": {
                          "constant_value": "log/"
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_s3_bucket_metric.s3_bucket_metric",
                      "mode": "managed",
                      "type": "aws_s3_bucket_metric",
                      "name": "s3_bucket_metric",
                      "provider_config_key": "aws",
                      "expressions": {
                        "bucket": {
                          "references": [
                            "aws_s3_bucket.s3_bucket.id",
                            "aws_s3_bucket.s3_bucket"
                          ]
                        },
                        "name": {
                          "constant_value": "EntireBucket"
                        }
                      },
                      "schema_version": 0,
                      "count_expression": {
                        "references": [
                          "var.enable_bucket_metric"
                        ]
                      }
                    },
                    {
                      "address": "aws_s3_bucket_object_lock_configuration.bucket_object_lock",
                      "mode": "managed",
                      "type": "aws_s3_bucket_object_lock_configuration",
                      "name": "bucket_object_lock",
                      "provider_config_key": "aws",
                      "expressions": {
                        "bucket": {
                          "references": [
                            "aws_s3_bucket.s3_bucket.id",
                            "aws_s3_bucket.s3_bucket"
                          ]
                        },
                        "rule": [
                          {
                            "default_retention": [
                              {
                                "days": {
                                  "references": [
                                    "var.object_lock_retention_days"
                                  ]
                                },
                                "mode": {
                                  "constant_value": "COMPLIANCE"
                                }
                              }
                            ]
                          }
                        ]
                      },
                      "schema_version": 0,
                      "count_expression": {
                        "references": [
                          "var.operational_backup",
                          "var.object_lock_retention_days"
                        ]
                      },
                      "depends_on": [
                        "aws_s3_bucket_versioning.bucket_versioning"
                      ]
                    },
                    {
                      "address": "aws_s3_bucket_policy.bucket_policy",
                      "mode": "managed",
                      "type": "aws_s3_bucket_policy",
                      "name": "bucket_policy",
                      "provider_config_key": "aws",
                      "expressions": {
                        "bucket": {
                          "references": [
                            "aws_s3_bucket.s3_bucket.id",
                            "aws_s3_bucket.s3_bucket"
                          ]
                        },
                        "policy": {
                          "references": [
                            "data.aws_iam_policy_document.combined.json",
                            "data.aws_iam_policy_document.combined"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_s3_bucket_public_access_block.public_access_block",
                      "mode": "managed",
                      "type": "aws_s3_bucket_public_access_block",
                      "name": "public_access_block",
                      "provider_config_key": "aws",
                      "expressions": {
                        "block_public_acls": {
                          "constant_value": true
                        },
                        "block_public_policy": {
                          "constant_value": true
                        },
                        "bucket": {
                          "references": [
                            "aws_s3_bucket.s3_bucket.id",
                            "aws_s3_bucket.s3_bucket"
                          ]
                        },
                        "ignore_public_acls": {
                          "constant_value": true
                        },
                        "restrict_public_buckets": {
                          "constant_value": true
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "aws_s3_bucket_versioning.bucket_versioning",
                      "mode": "managed",
                      "type": "aws_s3_bucket_versioning",
                      "name": "bucket_versioning",
                      "provider_config_key": "aws",
                      "expressions": {
                        "bucket": {
                          "references": [
                            "aws_s3_bucket.s3_bucket.id",
                            "aws_s3_bucket.s3_bucket"
                          ]
                        },
                        "versioning_configuration": [
                          {
                            "status": {
                              "constant_value": "Enabled"
                            }
                          }
                        ]
                      },
                      "schema_version": 0,
                      "count_expression": {
                        "references": [
                          "var.operational_backup"
                        ]
                      }
                    },
                    {
                      "address": "data.aws_iam_policy_document.allow_prisma",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "allow_prisma",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "s3:GetLifecycleConfiguration",
                                "s3:GetReplicationConfiguration",
                                "s3:GetAccelerateConfiguration",
                                "s3:GetAnalyticsConfiguration",
                                "s3:GetBucketAcl",
                                "s3:GetBucketCORS",
                                "s3:GetBucketLocation",
                                "s3:GetBucketLogging",
                                "s3:GetBucketObjectLockConfiguration",
                                "s3:GetBucketOwnershipControls",
                                "s3:GetBucketPolicy",
                                "s3:GetBucketPolicyStatus",
                                "s3:GetBucketPublicAccessBlock",
                                "s3:GetBucketTagging",
                                "s3:GetBucketVersioning",
                                "s3:GetBucketWebsite",
                                "s3:GetEncryptionConfiguration",
                                "s3:GetAccelerateConfiguration",
                                "s3:GetAnalyticsConfiguration",
                                "s3:GetBucket*",
                                "s3:GetEncryptionConfiguration",
                                "s3:GetInventoryConfiguration",
                                "s3:GetLifecycleConfiguration",
                                "s3:GetMetricsConfiguration",
                                "s3:GetReplicationConfiguration",
                                "s3:ListBucket"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "references": [
                                    "var.aws_account_id"
                                  ]
                                },
                                "type": {
                                  "constant_value": "AWS"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket"
                              ]
                            },
                            "sid": {
                              "constant_value": "AllowPrisma"
                            }
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.allow_prisma_object",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "allow_prisma_object",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "s3:GetObjectAcl",
                                "s3:GetObjectTagging",
                                "s3:GetObjectVersionAcl"
                              ]
                            },
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "references": [
                                    "var.aws_account_id"
                                  ]
                                },
                                "type": {
                                  "constant_value": "AWS"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket"
                              ]
                            },
                            "sid": {
                              "constant_value": "AllowPrismaObject"
                            }
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.allow_public_through_f5",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "allow_public_through_f5",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "s3:GetObject"
                              ]
                            },
                            "condition": [
                              {
                                "test": {
                                  "constant_value": "StringEquals"
                                },
                                "values": {
                                  "constant_value": [
                                    "vpc-0fbd9e814ef60d4ac"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:SourceVpc"
                                }
                              },
                              {
                                "test": {
                                  "constant_value": "IpAddress"
                                },
                                "values": {
                                  "constant_value": [
                                    "10.68.98.160/27",
                                    "10.68.98.128/27"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:VpcSourceIp"
                                }
                              }
                            ],
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "constant_value": [
                                    "*"
                                  ]
                                },
                                "type": {
                                  "constant_value": "*"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket",
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket"
                              ]
                            },
                            "sid": {
                              "constant_value": "AllowPublicThroughF5"
                            }
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.allow_ssl_only",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "allow_ssl_only",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "s3:*"
                              ]
                            },
                            "condition": [
                              {
                                "test": {
                                  "constant_value": "Bool"
                                },
                                "values": {
                                  "constant_value": [
                                    "false"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:SecureTransport"
                                }
                              }
                            ],
                            "effect": {
                              "constant_value": "Deny"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "constant_value": [
                                    "*"
                                  ]
                                },
                                "type": {
                                  "constant_value": "*"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket",
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket"
                              ]
                            },
                            "sid": {
                              "constant_value": "AllowSSLOnly"
                            }
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.allow_vpc_source",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "allow_vpc_source",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "s3:*"
                              ]
                            },
                            "condition": [
                              {
                                "test": {
                                  "constant_value": "StringEquals"
                                },
                                "values": {
                                  "constant_value": [
                                    "638883080465"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:VpceAccount"
                                }
                              }
                            ],
                            "effect": {
                              "constant_value": "Allow"
                            },
                            "principals": [
                              {
                                "identifiers": {
                                  "constant_value": [
                                    "*"
                                  ]
                                },
                                "type": {
                                  "constant_value": "*"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket",
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket"
                              ]
                            },
                            "sid": {
                              "constant_value": "AllowActionsFromInsideVPC"
                            }
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.combined",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "combined",
                      "provider_config_key": "aws",
                      "expressions": {
                        "source_policy_documents": {
                          "references": [
                            "data.aws_iam_policy_document.combined_custom.json",
                            "data.aws_iam_policy_document.combined_custom",
                            "data.aws_iam_policy_document.allow_prisma.json",
                            "data.aws_iam_policy_document.allow_prisma",
                            "data.aws_iam_policy_document.allow_prisma_object.json",
                            "data.aws_iam_policy_document.allow_prisma_object",
                            "data.aws_iam_policy_document.deny_not_principals.json",
                            "data.aws_iam_policy_document.deny_not_principals",
                            "data.aws_iam_policy_document.allow_ssl_only.json",
                            "data.aws_iam_policy_document.allow_ssl_only",
                            "data.aws_iam_policy_document.allow_vpc_source.json",
                            "data.aws_iam_policy_document.allow_vpc_source",
                            "var.allow_public_through_f5",
                            "data.aws_iam_policy_document.allow_public_through_f5.json",
                            "data.aws_iam_policy_document.allow_public_through_f5"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.combined_custom",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "combined_custom",
                      "provider_config_key": "aws",
                      "expressions": {
                        "source_policy_documents": {
                          "references": [
                            "var.policies",
                            "data.aws_iam_policy_document.custom_policy_document"
                          ]
                        }
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_iam_policy_document.custom_iam_policy_document",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "custom_iam_policy_document",
                      "provider_config_key": "aws",
                      "schema_version": 0,
                      "for_each_expression": {
                        "references": [
                          "var.iam_policies"
                        ]
                      }
                    },
                    {
                      "address": "data.aws_iam_policy_document.custom_policy_document",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "custom_policy_document",
                      "provider_config_key": "aws",
                      "schema_version": 0,
                      "for_each_expression": {
                        "references": [
                          "var.policies"
                        ]
                      }
                    },
                    {
                      "address": "data.aws_iam_policy_document.deny_not_principals",
                      "mode": "data",
                      "type": "aws_iam_policy_document",
                      "name": "deny_not_principals",
                      "provider_config_key": "aws",
                      "expressions": {
                        "statement": [
                          {
                            "actions": {
                              "constant_value": [
                                "s3:*"
                              ]
                            },
                            "condition": [
                              {
                                "test": {
                                  "constant_value": "StringNotEquals"
                                },
                                "values": {
                                  "constant_value": [
                                    "638883080465"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:VpceAccount"
                                }
                              },
                              {
                                "test": {
                                  "constant_value": "NotIpAddress"
                                },
                                "values": {
                                  "constant_value": [
                                    "10.68.98.160/27",
                                    "10.68.98.128/27"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:VpcSourceIp"
                                }
                              },
                              {
                                "test": {
                                  "constant_value": "StringNotEquals"
                                },
                                "values": {
                                  "references": [
                                    "var.network_exposure",
                                    "var.aws_account_id",
                                    "var.aws_account_id",
                                    "var.deny_exception_principals"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:PrincipalArn"
                                }
                              },
                              {
                                "test": {
                                  "constant_value": "BoolIfExists"
                                },
                                "values": {
                                  "constant_value": [
                                    "false"
                                  ]
                                },
                                "variable": {
                                  "constant_value": "aws:PrincipalIsAWSService"
                                }
                              }
                            ],
                            "effect": {
                              "constant_value": "Deny"
                            },
                            "not_principals": [
                              {
                                "identifiers": {
                                  "references": [
                                    "var.network_exposure",
                                    "var.aws_account_id",
                                    "var.aws_account_id",
                                    "var.deny_exception_principals"
                                  ]
                                },
                                "type": {
                                  "constant_value": "AWS"
                                }
                              }
                            ],
                            "resources": {
                              "references": [
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket",
                                "aws_s3_bucket.s3_bucket.arn",
                                "aws_s3_bucket.s3_bucket"
                              ]
                            },
                            "sid": {
                              "constant_value": "DenyNotPrincipals"
                            }
                          }
                        ]
                      },
                      "schema_version": 0
                    },
                    {
                      "address": "data.aws_s3_bucket.bucket_s3_access_logs",
                      "mode": "data",
                      "type": "aws_s3_bucket",
                      "name": "bucket_s3_access_logs",
                      "provider_config_key": "aws",
                      "expressions": {
                        "bucket": {
                          "references": [
                            "var.bucket_s3_access_logs_name"
                          ]
                        }
                      },
                      "schema_version": 0
                    }
                  ],
                  "variables": {
                    "allow_public_through_f5": {
                      "default": false,
                      "description": "Flag to enable public traffic to s3 bucket through f5."
                    },
                    "aws_account_id": {},
                    "aws_region": {},
                    "bucket_s3_access_logs_name": {
                      "default": "",
                      "description": "Name of s3 bucket deplyed in your account for access logs"
                    },
                    "custom_tags": {
                      "description": "Tags specific for the application"
                    },
                    "deny_exception_principals": {
                      "default": [],
                      "description": "List of AWS principals: they will not be under deny all actions if traffic source is not vpc"
                    },
                    "department": {},
                    "enable_bucket_metric": {
                      "default": false,
                      "description": "Flag to enable pay to use metrics"
                    },
                    "env": {},
                    "iam_policies": {
                      "default": [],
                      "description": "List of iam policies to create."
                    },
                    "network_exposure": {
                      "default": "private",
                      "description": "Network exposure of s3 bucket."
                    },
                    "object_lock_retention_days": {
                      "default": 0,
                      "description": "If the value of this variable is > 0, it enables object lock for a number of days equal to the value"
                    },
                    "operational_backup": {
                      "default": null,
                      "description": "operational_backup activates versioning and lifecycle management."
                    },
                    "policies": {
                      "default": [],
                      "description": "List of policies be added to the bucket policy"
                    },
                    "scope": {}
                  }
                },
                "version_constraint": "1.1.0"
              }
            },
            "variables": {
              "custom_tags_glue": {
                "default": {},
                "description": "Tags specific for the application"
              },
              "deny_exception_principals": {
                "default": [],
                "description": "List of AWS principals: they will not be under deny all actions if traffic source is not vpc"
              },
              "department": {
                "description": "The department name"
              },
              "env": {
                "description": "The department name"
              },
              "glue_crawler_iam_policies": {
                "default": [],
                "description": "Custom IAM policies list for Glue crawler"
              },
              "glue_crawlers": {
                "default": {},
                "description": "Map of Glue Crawlers to create (key = crawler logical name)"
              },
              "glue_databases": {
                "description": "Configurazione dei Glue Databases e delle relative tabelle"
              },
              "glue_iam_policies": {
                "default": [],
                "description": "Custom IAM policies list for Glue module"
              },
              "glue_version": {
                "default": "5.0",
                "description": "Glue version"
              },
              "lineage_configuration": {
                "default": null,
                "description": "Lineage configuration"
              },
              "number_of_workers": {
                "default": 2,
                "description": "Number of workers"
              },
              "s3_bucket_artifacts": {
                "description": "Configurazione del bucket 'S3 Artifacts'"
              },
              "schedule": {
                "default": null,
                "description": "Cron expression for crawler schedule"
              },
              "schema_change_policy": {
                "default": null,
                "description": "Schema change policy settings"
              },
              "scope": {
                "description": "The department name"
              },
              "table_prefix": {
                "default": null,
                "description": "Optional table prefix"
              },
              "worker_type": {
                "default": "G.1X",
                "description": "Worker type"
              }
            }
          }
        }
      },
      "variables": {
        "aws_region": {},
        "custom_tags_glue": {
          "default": {},
          "description": "Custom tags to apply to Glue resources"
        },
        "custom_tags_lambda": {
          "default": {},
          "description": "Custom tags to apply to Lambda resources"
        },
        "deny_exception_principals": {
          "default": [],
          "description": "List of AWS principals: they will not be under deny"
        },
        "department": {
          "description": "The department name"
        },
        "env": {
          "description": "The environment name"
        },
        "glue_crawler_iam_policies": {
          "description": "List of custom IAM policy definitions to attach to the Glue Crawler execution role created by the Glue Building Block"
        },
        "glue_crawlers": {
          "default": {},
          "description": "Glue Crawlers"
        },
        "glue_database_iam_policies": {
          "description": "List of custom IAM policy definitions to attach to the Glue Data Catalog database operations created by the Glue Building Block"
        },
        "glue_databases": {
          "description": "Configuration of the Glue databases and their related tables"
        },
        "glue_iam_policies": {
          "description": "List of custom IAM policy definitions to attach to the Glue Job execution role created by the Glue Building Block"
        },
        "glue_version": {
          "default": "5.0",
          "description": "AWS Glue version for the Glue Job"
        },
        "lambda_function_id": {
          "description": "The ID of the Lambda function"
        },
        "lambda_handler": {
          "description": "The handler for the Lambda function"
        },
        "lambda_memory_size": {
          "description": "The amount of memory allocated to the Lambda function"
        },
        "lambda_runtime": {
          "description": "The runtime environment for the Lambda function"
        },
        "lineage_configuration": {
          "description": "Glue Crawler lineage configuration"
        },
        "network_exposure": {
          "default": "hybrid",
          "description": "Network exposure mode for S3 Buckets"
        },
        "number_of_workers": {
          "default": 2,
          "description": "Number of workers allocated to the Glue Job"
        },
        "s3_bucket_artifacts": {
          "description": "Configuration of the 'S3 Artifacts' bucket"
        },
        "schedule": {
          "description": "Glue Crawler schedule expression"
        },
        "schema_change_policy": {
          "description": "Glue Crawler schema change policy configuration (delete/update behavior)"
        },
        "scope": {
          "description": "The scope name"
        },
        "script_location": {
          "default": "",
          "description": "S3 URI (or path) to the Glue Job script (e.g. s3://bucket/path/script.py)"
        },
        "subnet_ids": {
          "description": "Subnet IDs"
        },
        "table_prefix": {
          "default": "",
          "description": "Prefix to prepend to tables created/updated by the Glue Crawler"
        },
        "vpc_id": {
          "description": "VPC ID"
        },
        "worker_type": {
          "default": "G.1X",
          "description": "AWS Glue worker type for the Glue Job (e.g. G.1X, G.2X, G.4X, etc.)"
        }
      }
    }
  },
  "relevant_attributes": [
    {
      "resource": "module.blueprint.module.glue_catalog_database[\"raw_db\"].data.aws_iam_policy_document.custom_iam_policy_document",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].data.aws_iam_policy_document.assume_role",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.data.aws_caller_identity.current",
      "attribute": [
        "account_id"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.data.aws_iam_policy_document.glue_resource_policy_doc",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket.s3_bucket",
      "attribute": [
        "arn"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_catalog_database[\"raw_db\"].aws_iam_policy.iam_policy",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_s3_object.glue_etl_script",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_iam_role.role",
      "attribute": [
        "arn"
      ]
    },
    {
      "resource": "module.blueprint.data.aws_region.current",
      "attribute": [
        "region"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_prisma",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].data.aws_iam_policy_document.combined",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_vpc_source",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_iam_role.role",
      "attribute": [
        "name"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_glue_crawler.crawler",
      "attribute": [
        "database_name"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.aws_iam_policy.iam_policy",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_iam_role.role",
      "attribute": [
        "id"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_catalog_database.data.aws_iam_policy_document.custom_iam_policy_document",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_glue_job.job",
      "attribute": [
        "default_arguments"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.data.aws_iam_policy_document.assume_role",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_iam_role.role",
      "attribute": [
        "id"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_catalog_database.aws_glue_catalog_database.catalog",
      "attribute": [
        "name"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.data.aws_iam_policy_document.glue_job_policy",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.data.aws_caller_identity.current",
      "attribute": [
        "arn"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_prisma_object",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_catalog_database[\"raw_db\"].aws_glue_catalog_database.catalog",
      "attribute": [
        "name"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.combined",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_iam_role_policy.glue_job_permissions",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_job.data.aws_iam_policy_document.custom_iam_policy_document",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_glue_job.job",
      "attribute": [
        "timeout"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.deny_not_principals",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_glue_job.job",
      "attribute": [
        "command"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_iam_role.role",
      "attribute": [
        "assume_role_policy"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_glue_crawler.crawler",
      "attribute": [
        "name"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_iam_role.role",
      "attribute": [
        "arn"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_glue_security_configuration.this",
      "attribute": [
        "name"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_public_through_f5",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_s3_bucket.bucket_s3_access_logs",
      "attribute": [
        "id"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_catalog_database.aws_iam_policy.iam_policy",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_glue_job.job",
      "attribute": [
        "name"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.data.aws_iam_policy_document.glue_job_combined_policy",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.combined_custom",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].aws_glue_crawler.crawler",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_glue_job.job",
      "attribute": [
        "max_retries"
      ]
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_glue_job.job",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.glue_job.aws_iam_role.role",
      "attribute": [
        "name"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.custom_iam_policy_document",
      "attribute": []
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.data.aws_iam_policy_document.allow_ssl_only",
      "attribute": [
        "json"
      ]
    },
    {
      "resource": "module.blueprint.module.s3_bucket_artifacts.aws_s3_bucket.s3_bucket",
      "attribute": [
        "id"
      ]
    }
  ],
  "checks": [
    {
      "address": {
        "kind": "var",
        "module": "module.blueprint.module.glue_catalog_database",
        "name": "custom_tags",
        "to_display": "module.blueprint.module.glue_catalog_database.var.custom_tags"
      },
      "status": "pass",
      "instances": [
        {
          "address": {
            "module": "module.blueprint.module.glue_catalog_database[\"raw_db\"]",
            "to_display": "module.blueprint.module.glue_catalog_database[\"raw_db\"].var.custom_tags"
          },
          "status": "pass"
        }
      ]
    },
    {
      "address": {
        "kind": "var",
        "module": "module.blueprint.module.glue_crawler",
        "name": "custom_tags",
        "to_display": "module.blueprint.module.glue_crawler.var.custom_tags"
      },
      "status": "pass",
      "instances": [
        {
          "address": {
            "module": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"]",
            "to_display": "module.blueprint.module.glue_crawler[\"crawler_l0_raw\"].var.custom_tags"
          },
          "status": "pass"
        }
      ]
    },
    {
      "address": {
        "kind": "var",
        "module": "module.blueprint.module.glue_job",
        "name": "custom_tags",
        "to_display": "module.blueprint.module.glue_job.var.custom_tags"
      },
      "status": "pass",
      "instances": [
        {
          "address": {
            "module": "module.blueprint.module.glue_job",
            "to_display": "module.blueprint.module.glue_job.var.custom_tags"
          },
          "status": "pass"
        }
      ]
    },
    {
      "address": {
        "kind": "var",
        "module": "module.blueprint.module.glue_job",
        "name": "job_type",
        "to_display": "module.blueprint.module.glue_job.var.job_type"
      },
      "status": "pass",
      "instances": [
        {
          "address": {
            "module": "module.blueprint.module.glue_job",
            "to_display": "module.blueprint.module.glue_job.var.job_type"
          },
          "status": "pass"
        }
      ]
    },
    {
      "address": {
        "kind": "var",
        "module": "module.blueprint.module.s3_bucket_artifacts",
        "name": "custom_tags",
        "to_display": "module.blueprint.module.s3_bucket_artifacts.var.custom_tags"
      },
      "status": "pass",
      "instances": [
        {
          "address": {
            "module": "module.blueprint.module.s3_bucket_artifacts",
            "to_display": "module.blueprint.module.s3_bucket_artifacts.var.custom_tags"
          },
          "status": "pass"
        }
      ]
    },
    {
      "address": {
        "kind": "var",
        "module": "module.blueprint.module.s3_bucket_artifacts",
        "name": "network_exposure",
        "to_display": "module.blueprint.module.s3_bucket_artifacts.var.network_exposure"
      },
      "status": "pass",
      "instances": [
        {
          "address": {
            "module": "module.blueprint.module.s3_bucket_artifacts",
            "to_display": "module.blueprint.module.s3_bucket_artifacts.var.network_exposure"
          },
          "status": "pass"
        }
      ]
    },
    {
      "address": {
        "kind": "var",
        "module": "module.blueprint",
        "name": "custom_tags_glue",
        "to_display": "module.blueprint.var.custom_tags_glue"
      },
      "status": "pass",
      "instances": [
        {
          "address": {
            "module": "module.blueprint",
            "to_display": "module.blueprint.var.custom_tags_glue"
          },
          "status": "pass"
        }
      ]
    }
  ],
  "timestamp": "2026-02-16T09:13:13Z",
  "applyable": true,
  "complete": true,
  "errored": false
}
