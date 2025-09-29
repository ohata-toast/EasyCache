# イベント

**Database > EasyCache > コンソール利用ガイド > イベント**

イベントとは、Valkeyまたはユーザーによって発生した重要な出来事を意味します。イベントは、イベントタイプ、発生日時、ソース、メッセージで構成されます。イベントはコンソールで照会でき、サブスクリプションを通じてメール、SMSでイベント発生の通知を受け取ることができます。イベントのタイプと発生可能なイベントは次のとおりです。

* 現在提供しているイベントタイプ及びイベントコード

| イベントタイプ | イベントコード | サブスクリプション | 説明 |
| - | - | - | - |
| CACHE | APPLY_LATEST_PARAMETER_GROUP_START | はい | 最新パラメータグループの適用を開始 |
| CACHE | APPLY_LATEST_PARAMETER_GROUP_END | はい | 最新パラメータグループの適用が完了 |
| CACHE | APPLY_LATEST_PARAMETER_GROUP_FAILED | はい | 最新パラメータグループの適用に失敗 |
| CACHE | AUTO_BACKUP_ACTIVATION_START | はい | 自動バックアップの有効化を開始 |
| CACHE | AUTO_BACKUP_ACTIVATION_END | はい | 自動バックアップの有効化が完了 |
| CACHE | AUTO_BACKUP_ACTIVATION_FAILED | はい | 自動バックアップの有効化に失敗 |
| CACHE | AUTO_BACKUP_DEACTIVATION_START | はい | 自動バックアップの無効化を開始 |
| CACHE | AUTO_BACKUP_DEACTIVATION_END | はい | 自動バックアップの無効化が完了 |
| CACHE | AUTO_BACKUP_DEACTIVATION_FAILED | はい | 自動バックアップの無効化に失敗 |
| CACHE | BACKUP_START | はい | バックアップを開始 |
| CACHE | BACKUP_END | はい | バックアップが完了 |
| CACHE | BACKUP_FAILED | はい | バックアップに失敗 |
| CACHE | BACKUP_MIGRATE_START | いいえ | バックアップの移行を開始 |
| CACHE | BACKUP_MIGRATE_END | いいえ | バックアップの移行が完了 |
| CACHE | BACKUP_MIGRATE_DOWNLOAD_FAILED | いいえ | バックアップ移行のダウンロードに失敗 |
| CACHE | BACKUP_MIGRATE_RDB_CHECK_FAILED | いいえ | バックアップ移行のRDBチェックに失敗 |
| CACHE | BACKUP_MIGRATE_RDB_CHECKSUM_FAILED | いいえ | バックアップ移行のRDBチェックサムに失敗 |
| CACHE | BACKUP_MIGRATE_RDB_MEMORY_FAILED | いいえ | バックアップ移行のRDBメモリに失敗 |
| CACHE | BACKUP_MIGRATE_RDB_TYPE_FAILED | いいえ | バックアップ移行のRDBタイプに失敗 |
| CACHE | BACKUP_MIGRATE_RDB_VERSION_FAILED | いいえ | バックアップ移行のRDBバージョンに失敗 |
| CACHE | BACKUP_MIGRATE_REPLICA_CHECK_FAILED | いいえ | バックアップ移行のレプリカチェックに失敗 |
| CACHE | BACKUP_MIGRATE_RESTART_FAILED | いいえ | バックアップ移行の再起動に失敗 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_START | はい | 既存のキャッシュへのバックアップ復元を開始 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_END | はい | 既存のキャッシュへのバックアップ復元が完了 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_FAILED | はい | 既存のキャッシュへのバックアップ復元に失敗 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_DOWNLOAD_FAILED | はい | 既存のキャッシュへのバックアップ復元ダウンロードに失敗 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_RDB_CHECK_FAILED | はい | 既存のキャッシュへのバックアップ復元RDBチェックに失敗 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_RDB_CHECKSUM_FAILED | はい | 既存のキャッシュへのバックアップ復元RDBチェックサムに失敗 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_RDB_MEMORY_FAILED | はい | 既存のキャッシュへのバックアップ復元RDBメモリに失敗 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_RDB_TYPE_FAILED | はい | 既存のキャッシュへのバックアップ復元RDBタイプに失敗 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_RDB_VERSION_FAILED | はい | 既存のキャッシュへのバックアップ復元RDBバージョンに失敗 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_REPLICA_CHECK_FAILED | はい | 既存のキャッシュへのバックアップ復元レプリカチェックに失敗 |
| CACHE | BACKUP_RESTORE_EXISTING_CACHE_RESTART_FAILED | はい | 既存のキャッシュへのバックアップ復元再起動に失敗 |
| CACHE | BACKUP_RESTORE_NEW_CACHE_START | はい | 新規キャッシュへのバックアップ復元を開始 |
| CACHE | BACKUP_RESTORE_NEW_CACHE_END | はい | 新規キャッシュへのバックアップ復元が完了 |
| CACHE | BACKUP_RESTORE_NEW_CACHE_FAILED | はい | 新規キャッシュへのバックアップ復元に失敗 |
| CACHE | CACHE_CERTIFICATE_UPDATE_START | はい | キャッシュ証明書の更新を開始 |
| CACHE | CACHE_CERTIFICATE_UPDATE_END | はい | キャッシュ証明書の更新が完了 |
| CACHE | CACHE_CERTIFICATE_UPDATE_FAILED | はい | キャッシュ証明書の更新に失敗 |
| CACHE | CACHE_CREATION_START | はい | キャッシュの作成を開始 |
| CACHE | CACHE_CREATION_END | はい | キャッシュの作成が完了 |
| CACHE | CACHE_CREATION_FAILED | はい | キャッシュの作成に失敗 |
| CACHE | CACHE_DATA_EXPORTING_START | はい | キャッシュデータのエクスポートを開始 |
| CACHE | CACHE_DATA_EXPORTING_END | はい | キャッシュデータのエクスポートが完了 |
| CACHE | CACHE_DATA_EXPORTING_FAILED | はい | キャッシュデータのエクスポートに失敗 |
| CACHE | CACHE_DATA_EXPORTING_RDB_CREATE_FAILED | はい | キャッシュデータエクスポートのRDB作成に失敗 |
| CACHE | CACHE_DATA_EXPORTING_SETTING_FAILED | はい | キャッシュデータエクスポートの設定に失敗 |
| CACHE | CACHE_DATA_EXPORTING_UPLOAD_FAILED | はい | キャッシュデータエクスポートのアップロードに失敗 |
| CACHE | CACHE_DATA_IMPORTING_START | はい | キャッシュデータのインポートを開始 |
| CACHE | CACHE_DATA_IMPORTING_END | はい | キャッシュデータのインポートが完了 |
| CACHE | CACHE_DATA_IMPORTING_FAILED | はい | キャッシュデータのインポートに失敗 |
| CACHE | CACHE_DATA_IMPORTING_DOWNLOAD_FAILED | はい | キャッシュデータインポートのダウンロードに失敗 |
| CACHE | CACHE_DATA_IMPORTING_RDB_CHECK_FAILED | はい | キャッシュデータインポートのRDBチェックに失敗 |
| CACHE | CACHE_DATA_IMPORTING_RDB_CHECKSUM_FAILED | はい | キャッシュデータインポートのRDBチェックサムに失敗 |
| CACHE | CACHE_DATA_IMPORTING_RDB_MEMORY_FAILED | はい | キャッシュデータインポートのRDBメモリに失敗 |
| CACHE | CACHE_DATA_IMPORTING_RDB_TYPE_FAILED | はい | キャッシュデータインポートのRDBタイプに失敗 |
| CACHE | CACHE_DATA_IMPORTING_RDB_VERSION_FAILED | はい | キャッシュデータインポートのRDBバージョンに失敗 |
| CACHE | CACHE_DATA_IMPORTING_REPLICA_CHECK_FAILED | はい | キャッシュデータインポートのレプリカチェックに失敗 |
| CACHE | CACHE_DATA_IMPORTING_RESTART_FAILED | はい | キャッシュデータインポートの再起動に失敗 |
| CACHE | CACHE_DATA_IMPORTING_SETTING_FAILED | はい | キャッシュデータインポートの設定に失敗 |
| CACHE | CACHE_DELETION_START | はい | キャッシュの削除を開始 |
| CACHE | CACHE_DELETION_END | はい | キャッシュの削除が完了 |
| CACHE | CACHE_DELETION_FAILED | はい | キャッシュの削除に失敗 |
| CACHE | CACHE_DELETION_PROTECTION_DISABLING_START | はい | キャッシュ削除保護の無効化を開始 |
| CACHE | CACHE_DELETION_PROTECTION_DISABLING_END | はい | キャッシュ削除保護の無効化が完了 |
| CACHE | CACHE_DELETION_PROTECTION_DISABLING_FAILED | はい | キャッシュ削除保護の無効化に失敗 |
| CACHE | CACHE_DELETION_PROTECTION_ENABLING_START | はい | キャッシュ削除保護の有効化を開始 |
| CACHE | CACHE_DELETION_PROTECTION_ENABLING_END | はい | キャッシュ削除保護の有効化が完了 |
| CACHE | CACHE_DELETION_PROTECTION_ENABLING_FAILED | はい | キャッシュ削除保護の有効化に失敗 |
| CACHE | CACHE_DETAIL_MODIFICATION_START | はい | キャッシュ詳細の修正を開始 |
| CACHE | CACHE_DETAIL_MODIFICATION_END | はい | キャッシュ詳細の修正が完了 |
| CACHE | CACHE_DETAIL_MODIFICATION_FAILED | はい | キャッシュ詳細の修正に失敗 |
| CACHE | CACHE_FLAVOR_MODIFICATION_START | はい | キャッシュ仕様の変更を開始 |
| CACHE | CACHE_FLAVOR_MODIFICATION_END | はい | キャッシュ仕様の変更が完了 |
| CACHE | CACHE_FLAVOR_MODIFICATION_FAILED | はい | キャッシュ仕様の変更に失敗 |
| CACHE | CACHE_HIGH_AVAILABILITY_REPAIR_START | はい | キャッシュ高可用性の復旧を開始 |
| CACHE | CACHE_HIGH_AVAILABILITY_REPAIR_END | はい | キャッシュ高可用性の復旧が完了 |
| CACHE | CACHE_HIGH_AVAILABILITY_REPAIR_FAILED | はい | キャッシュ高可用性の復旧に失敗 |
| CACHE | CACHE_MASTER_ROLE_CHANGING_START | はい | キャッシュマスターロールの変更を開始 |
| CACHE | CACHE_MASTER_ROLE_CHANGING_END | はい | キャッシュマスターロールの変更が完了 |
| CACHE | CACHE_MASTER_ROLE_CHANGING_FAILED | はい | キャッシュマスターロールの変更に失敗 |
| CACHE | CACHE_MODIFICATION_START | はい | キャッシュの修正を開始 |
| CACHE | CACHE_MODIFICATION_END | はい | キャッシュの修正が完了 |
| CACHE | CACHE_MODIFICATION_FAILED | はい | キャッシュの修正に失敗 |
| CACHE | CACHE_RESTART_START | はい | キャッシュの再起動を開始 |
| CACHE | CACHE_RESTART_END | はい | キャッシュの再起動が完了 |
| CACHE | CACHE_RESTART_FAILED | はい | キャッシュの再起動に失敗 |
| CACHE | CACHE_STARTING_START | はい | キャッシュの起動を開始 |
| CACHE | CACHE_STARTING_END | はい | キャッシュの起動が完了 |
| CACHE | CACHE_STARTING_FAILED | はい | キャッシュの起動に失敗 |
| CACHE | CACHE_STOPPING_START | はい | キャッシュの停止を開始 |
| CACHE | CACHE_STOPPING_END | はい | キャッシュの停止が完了 |
| CACHE | CACHE_STOPPING_FAILED | はい | キャッシュの停止に失敗 |
| CACHE | CACHE_UPGRADE_START | はい | キャッシュのアップグレードを開始 |
| CACHE | CACHE_UPGRADE_END | はい | キャッシュのアップグレードが完了 |
| CACHE | CACHE_UPGRADE_FAILED | はい | キャッシュのアップグレードに失敗 |
| CACHE | CACHE_UPGRADE_HA_UPGRADE_FAILED | はい | キャッシュアップグレードHAに失敗 |
| CACHE | CACHE_UPGRADE_MASTER_UPGRADE_FAILED | はい | キャッシュアップグレードマスターに失敗 |
| CACHE | CACHE_UPGRADE_REPLICA_PROMOTE_FAILED | はい | キャッシュアップグレードレプリカの昇格に失敗 |
| CACHE | CACHE_UPGRADE_REPLICA_UPGRADE_FAILED | はい | キャッシュアップグレードレプリカに失敗 |
| CACHE | FAILOVER_DNS_FAILED | いいえ | DNS更新に失敗 |
| CACHE | FAILOVER_DNSFAIL | はい | フェイルオーバーDNSに失敗 |
| CACHE | FAILOVER_EXECUTED | はい | フェイルオーバーが発生 |
| CACHE | FLOATING_IP_ATTACHING_START | はい | フローティングIPの接続を開始 |
| CACHE | FLOATING_IP_ATTACHING_END | はい | フローティングIPの接続が完了 |
| CACHE | FLOATING_IP_ATTACHING_FAILED | はい | フローティングIPの接続に失敗 |
| CACHE | FLOATING_IP_DETACHING_START | はい | フローティングIPの解除を開始 |
| CACHE | FLOATING_IP_DETACHING_END | はい | フローティングIPの解除が完了 |
| CACHE | FLOATING_IP_DETACHING_FAILED | はい | フローティングIPの解除に失敗 |
| CACHE | HA_NODE_CREATION_START | はい | HAノードの作成を開始 |
| CACHE | HA_NODE_CREATION_END | はい | HAノードの作成が完了 |
| CACHE | HA_NODE_CREATION_FAILED | はい | HAノードの作成に失敗 |
| CACHE | HA_NODE_DELETION_START | はい | HAノードの削除を開始 |
| CACHE | HA_NODE_DELETION_END | はい | HAノードの削除が完了 |
| CACHE | NODE_OS_UPGRADE_START | はい | ノードOSのアップグレードを開始 |
| CACHE | NODE_OS_UPGRADE_END | はい | ノードOSのアップグレードが完了 |
| CACHE | NODE_OS_UPGRADE_FAILED | はい | ノードOSのアップグレードに失敗 |
| CACHE | READONLY_DOMAIN_ATTACHING_START | はい | 読み取り専用ドメインの接続を開始 |
| CACHE | READONLY_DOMAIN_ATTACHING_END | はい | 読み取り専用ドメインの接続が完了 |
| CACHE | READONLY_DOMAIN_ATTACHING_FAILED | はい | 読み取り専用ドメインの接続に失敗 |
| CACHE | READONLY_DOMAIN_DETACHING_START | はい | 読み取り専用ドメインの解除を開始 |
| CACHE | READONLY_DOMAIN_DETACHING_END | はい | 読み取り専用ドメインの解除が完了 |
| CACHE | READONLY_DOMAIN_DETACHING_FAILED | はい | 読み取り専用ドメインの解除に失敗 |
| CACHE | READONLY_DOMAIN_UPDATE_START | はい | 読み取り専用ドメインの更新を開始 |
| CACHE | READONLY_DOMAIN_UPDATE_END | はい | 読み取り専用ドメインの更新が完了 |
| CACHE | READONLY_DOMAIN_UPDATE_FAILED | はい | 読み取り専用ドメインの更新に失敗 |
| CACHE | SENTINEL_CREATION_START | いいえ | Sentinelノードの作成を開始 |
| CACHE | SENTINEL_CREATION_END | いいえ | Sentinelノードの作成が完了 |
| CACHE | SENTINEL_CREATION_FAILED | いいえ | Sentinelノードの作成に失敗 |
| CACHE | SENTINEL_DELETION_START | いいえ | Sentinelノードの削除を開始 |
| CACHE | SENTINEL_DELETION_END | いいえ | Sentinelノードの削除が完了 |
| CACHE | SENTINEL_DELETION_FAILED | いいえ | Sentinelノードの削除に失敗 |
| CACHE | SENTINEL_FAILOVER | いいえ | フェイルオーバーが発生 |
| CACHE | SENTINEL_FAILOVER_DNSFAIL | いいえ | フェイルオーバーDNSに失敗 |
| CACHE | SENTINEL_QUORUM_UPDATE_START | はい | Sentinelクォーラムの更新を開始 |
| CACHE | SENTINEL_QUORUM_UPDATE_END | はい | Sentinelクォーラムの更新が完了 |
| CACHE | SENTINEL_QUORUM_UPDATE_FAILED | はい | Sentinelクォーラムの更新に失敗 |
| CACHE | SLAVE_NODE_PROMOTION_START | はい | スレーブノードの昇格を開始 |
| CACHE | SLAVE_NODE_PROMOTION_END | はい | スレーブノードの昇格が完了 |
| CACHE | SLAVE_NODE_PROMOTION_FAILED | はい | スレーブノードの昇格に失敗 |
| NODE | NODE_DELETION_START | はい | ノードの削除を開始 |
| NODE | NODE_DELETION_END | はい | ノードの削除が完了 |
| NODE | NODE_DELETION_FAILED | はい | ノードの削除に失敗 |
| NODE | NODE_DOWN_DETECTED | はい | ノードが停止しました |
| NODE | NODE_FLAVOR_MODIFICATION_START | はい | ノード仕様の変更を開始 |
| NODE | NODE_FLAVOR_MODIFICATION_END | はい | ノード仕様の変更が完了 |
| NODE | NODE_FLAVOR_MODIFICATION_FAILED | はい | ノード仕様の変更に失敗 |
| NODE | NODE_PLANNED_MIGRATION_START | はい | ノード計画的移行を開始 |
| NODE | NODE_PLANNED_MIGRATION_END | はい | ノード計画的移行が完了 |
| NODE | NODE_PLANNED_MIGRATION_FAILED | はい | ノード計画的移行に失敗 |
| NODE | NODE_RECOVERED | はい | ノード実行中 |
| NODE | NODE_UPGRADE_START | はい | ノードエンジンのアップグレードを開始 |
| NODE | NODE_UPGRADE_END | はい | ノードエンジンのアップグレードが完了 |
| NODE | NODE_UPGRADE_FAILED | はい | ノードエンジンのアップグレードに失敗 |
| NODE | NODE_UPGRADE_DOWNLOAD_FAILED | はい | ノードエンジンアップグレードのダウンロードに失敗 |
| NODE | NODE_UPGRADE_PROFILE_UPDATE_FAILED | はい | ノードエンジンアップグレードのパラメータグループ更新に失敗 |
| NODE | NODE_UPGRADE_REDIS_N_SENTINEL_START_FAILED | はい | ノードエンジンアップグレードのサービス開始に失敗 |
| NODE | NODE_UPGRADE_REDIS_N_SENTINEL_STOP_FAILED | はい | ノードエンジンアップグレードのサービス停止に失敗 |
| NODE | NODE_UPGRADE_REDIS_UPGRADE_FAILED | はい | ノードエンジンアップグレードのRedisアップグレードに失敗 |
| NODE | NODE_UPGRADE_REPLICA_CHECK_FAILED | はい | ノードエンジンアップグレードのレプリカチェックに失敗 |
| NODE | NODE_UPGRADE_RPM_DELETE_FAILED | はい | ノードエンジンアップグレードのRPM削除に失敗 |
| NODE | NODE_UPGRADE_SENTINEL_START_FAILED | はい | ノードエンジンアップグレードのSentinel開始に失敗 |
| NODE | NODE_UPGRADE_SENTINEL_STOP_FAILED | はい | ノードエンジンアップグレードのSentinel停止に失敗 |
| NODE | SENTINEL_INSTANCE_RUNNING | いいえ | インスタンスの実行 |
| NODE | SENTINEL_INSTANCE_STOPPED | いいえ | インスタンスが停止しました |
| NODE | SLAVE_NODE_CREATION_START | はい | レプリケーションノードの作成を開始 |
| NODE | SLAVE_NODE_CREATION_END | はい | レプリケーションノードの作成が完了 |
| NODE | SLAVE_NODE_CREATION_FAILED | はい | レプリケーションノードの作成に失敗 |
| NODE | STATUS_CHANGED_DISABLED | いいえ | 無効 |
| NODE | STATUS_CHANGED_ENABLED | いいえ | 有効 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_CREATION_START | いいえ | DBセキュリティグループの作成を開始 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_CREATION_END | いいえ | DBセキュリティグループの作成が完了 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_CREATION_FAILED | いいえ | DBセキュリティグループの作成に失敗 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_DELETION_START | いいえ | DBセキュリティグループの削除を開始 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_DELETION_END | いいえ | DBセキュリティグループの削除が完了 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_DELETION_FAILED | いいえ | DBセキュリティグループの削除に失敗 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_MODIFICATION_START | いいえ | DBセキュリティグループの修正を開始 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_MODIFICATION_END | いいえ | DBセキュリティグループの修正が完了 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_MODIFICATION_FAILED | いいえ | DBセキュリティグループの修正に失敗 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_RULE_CREATION_START | いいえ | DBセキュリティグループのルール作成を開始 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_RULE_CREATION_END | いいえ | DBセキュリティグループのルール作成が完了 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_RULE_CREATION_FAILED | いいえ | DBセキュリティグループのルール作成に失敗 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_RULE_DELETION_START | いいえ | DBセキュリティグループのルール削除を開始 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_RULE_DELETION_END | いいえ | DBセキュリティグループのルール削除が完了 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_RULE_DELETION_FAILED | いいえ | DBセキュリティグループのルール削除に失敗 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_RULE_MODIFICATION_START | いいえ | DBセキュリティグループのルール修正を開始 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_RULE_MODIFICATION_END | いいえ | DBセキュリティグループのルール修正が完了 |
| DB_SECURITY_GROUP | DB_SECURITY_GROUP_RULE_MODIFICATION_FAILED | いいえ | DBセキュリティグループのルール修正に失敗 |
| PARAMETER_GROUP | PROFILE_UPDATE_START | いいえ | プロファイルの更新を開始 |
| PARAMETER_GROUP | PROFILE_UPDATE_END | いいえ | プロファイルの更新が完了 |
| PARAMETER_GROUP | PROFILE_UPDATE_FAILED | いいえ | プロファイルの更新に失敗 |
| MONITORING | METRIC_ALARM_TRIGGERED | はい | モニタリングアラームが発生 |

* 記録は残っていますが、これ以上新規作成されないイベントコード

| イベントタイプ | イベントコード | サブスクリプション | 説明 |
| - | - | - | - |
| CACHE | GROUP_CERTIFICATE_UPDATE_START | いいえ | グループ証明書の更新を開始 |
| CACHE | GROUP_CERTIFICATE_UPDATE_END | いいえ | グループ証明書の更新が完了 |
| CACHE | GROUP_CERTIFICATE_UPDATE_FAILED | いいえ | グループ証明書の更新に失敗 |
| CACHE | GROUP_CREATION_START | いいえ | グループの作成を開始 |
| CACHE | GROUP_CREATION_END | いいえ | グループの作成が完了 |
| CACHE | GROUP_CREATION_FAILED | いいえ | グループの作成に失敗 |
| CACHE | GROUP_DATA_EXPORTING_START | いいえ | グループデータのエクスポートを開始 |
| CACHE | GROUP_DATA_EXPORTING_END | いいえ | グループデータのエクスポートが完了 |
| CACHE | GROUP_DATA_EXPORTING_FAILED | いいえ | グループデータのエクスポートに失敗 |
| CACHE | GROUP_DATA_EXPORTING_RDB_CREATE_FAILED | いいえ | グループデータエクスポートのRDB作成に失敗 |
| CACHE | GROUP_DATA_EXPORTING_SETTING_FAILED | いいえ | グループデータエクスポートの設定に失敗 |
| CACHE | GROUP_DATA_EXPORTING_UPLOAD_FAILED | いいえ | グループデータエクスポートのアップロードに失敗 |
| CACHE | GROUP_DATA_IMPORTING_START | いいえ | グループデータのインポートを開始 |
| CACHE | GROUP_DATA_IMPORTING_END | いいえ | グループデータのインポートが完了 |
| CACHE | GROUP_DATA_IMPORTING_DOWNLOAD_FAILED | いいえ | グループデータインポートのダウンロードに失敗 |
| CACHE | GROUP_DATA_IMPORTING_RDB_CHECK_FAILED | いいえ | グループデータインポートのRDBチェックに失敗 |
| CACHE | GROUP_DATA_IMPORTING_RDB_CHECKSUM_FAILED | いいえ | グループデータインポートのRDBチェックサムに失敗 |
| CACHE | GROUP_DATA_IMPORTING_RDB_MEMORY_FAILED | いいえ | グループデータインポートのRDBメモリに失敗 |
| CACHE | GROUP_DATA_IMPORTING_RDB_TYPE_FAILED | いいえ | グループデータインポートのRDBタイプに失敗 |
| CACHE | GROUP_DATA_IMPORTING_RDB_VERSION_FAILED | いいえ | グループデータインポートのRDBバージョンに失敗 |
| CACHE | GROUP_DATA_IMPORTING_REPLICA_CHECK_FAILED | いいえ | グループデータインポートのレプリカチェックに失敗 |
| CACHE | GROUP_DATA_IMPORTING_RESTART_FAILED | いいえ | グループデータインポートの再起動に失敗 |
| CACHE | GROUP_DATA_IMPORTING_SETTING_FAILED | いいえ | グループデータインポートの設定に失敗 |
| CACHE | GROUP_DELETION_START | いいえ | グループの削除を開始 |
| CACHE | GROUP_DELETION_END | いいえ | グループの削除が完了 |
| CACHE | GROUP_DELETION_FAILED | いいえ | グループの削除に失敗 |
| CACHE | GROUP_FLAVOR_MODIFICATION_START | いいえ | グループ仕様の変更を開始 |
| CACHE | GROUP_FLAVOR_MODIFICATION_END | いいえ | グループ仕様の変更が完了 |
| CACHE | GROUP_FLAVOR_MODIFICATION_FAILED | いいえ | グループ仕様の変更に失敗 |
| CACHE | GROUP_MODIFICATION_START | いいえ | グループの修正を開始 |
| CACHE | GROUP_MODIFICATION_END | いいえ | グループの修正が完了 |
| CACHE | GROUP_MODIFICATION_FAILED | いいえ | グループの修正に失敗 |
| CACHE | GROUP_RESTART_START | いいえ | グループの再起動を開始 |
| CACHE | GROUP_RESTART_END | いいえ | グループの再起動が完了 |
| CACHE | GROUP_RESTART_FAILED | いいえ | グループの再起動に失敗 |
| CACHE | GROUP_UPGRADE_START | いいえ | グループのアップグレードを開始 |
| CACHE | GROUP_UPGRADE_END | いいえ | グループのアップグレードが完了 |
| CACHE | GROUP_UPGRADE_FAILED | いいえ | グループのアップグレードに失敗 |
| CACHE | GROUP_UPGRADE_HA_UPGRADE_FAILED | いいえ | グループアップグレードHAに失敗 |
| CACHE | GROUP_UPGRADE_MASTER_UPGRADE_FAILED | いいえ | グループアップグレードマスターに失敗 |
| CACHE | GROUP_UPGRADE_REPLICA_PROMOTE_FAILED | いいえ | グループアップグレードレプリカの昇格に失敗 |
| CACHE | GROUP_UPGRADE_REPLICA_UPGRADE_FAILED | いいえ | グループアップグレードレプリカに失敗 |


## イベントのサブスクリプション

イベントタイプ、コード、ソースで分類してイベントをサブスクライブできます。イベントタイプでサブスクライブすると、イベントタイプに含まれる全てのイベントコードの通知を受け取ります。通知が広範囲すぎる場合は、イベントコードとソースで細分化してサブスクライブできます。プロジェクトメンバーのみを通知対象ユーザーとして選択できます。デフォルトではメールでイベント通知が送信され、実名認証済みの携帯電話番号が登録されている場合にのみ、SMSで追加のイベント通知が送信されます。

![event1.PNG](https://static.toastoven.net/prod_easycache/25.09.27/event1.PNG)
![event2.PNG](https://static.toastoven.net/prod_easycache/25.09.27/event2.PNG)

❶: **イベントサブスクリプション登録**を押すと、イベントサブスクリプションを登録できるポップアップウィンドウが表示されます。
❷: サブスクライブするイベントタイプを選択します。イベントタイプによって選択できるイベントコードが変わります。
❸: イベントテンプレートを利用すると、テンプレートに予め定義されたイベントコードを一度に入力できます。
❹: サブスクライブするイベントコードを直接選択します。イベントテンプレートを使用した状態でイベントコードを変更すると、イベントテンプレートの項目が解除されます。
❺: サブスクライブするイベントソースを直接選択します。
❻: イベント通知を受け取るユーザーグループを選択します。
❼: 通知タイプを通じて通知を受け取る方法を選択します。
❽: 有効化するかどうかを選択します。有効化を**いいえ**に選択した場合、イベント発生通知は送信されません。