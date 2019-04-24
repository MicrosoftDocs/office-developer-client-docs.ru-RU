---
title: Свойство Database. Десигнмастерид (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a189d16880fccdc34c169aee61c6781e1d86afa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294934"
---
# <a name="databasedesignmasterid-property-dao"></a>Свойство Database. Десигнмастерид (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает 16-байтовое значение, которое уникально определяет основную реплику в наборе реплик (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Десигнмастерид

*выражение*: переменная, представляющая объект **Database**.

## <a name="remarks"></a>Замечания

Свойство **десигнмастерид** следует задавать только в том случае, если требуется переместить текущую основную реплику. При установке этого свойства в реплике устанавливается основная реплика.

> [!NOTE]
> Никогда не создавайте вторую основную реплику в наборе реплик. Наличие второй основной реплики может привести к потере данных.

В экстремальных обстоятельствах — например, если основная реплика удаляется или повреждается, можно задать это свойство в текущей реплике. Тем не менее, задание этого свойства в реплике при наличии другой основной реплики в наборе может разделить набор реплик на два набора ирреконЦилабле и предотвратить дальнейшую синхронизацию данных.

Если вы решили сделать реплику новой основной репликой для набора, синхронизируйте ее со всеми репликами в наборе реплик, прежде чем устанавливать свойство **десигнмастерид** в реплике. Реплика должна быть открыта в монопольном режиме, чтобы сделать ее основной.

Если вы сделаете реплику, предназначенную только для чтения, в основной реплике, Целевая реплика становится доступна для чтения и записи; Старая основная реплика также остается для чтения и записи.

Значение свойства **десигнмастерид** хранится в системной таблице мсисрепинфо.

## <a name="example"></a>Пример

В этом примере показано, как задать для свойства **десигнмастерид** значение свойства **replicaId** другой базы данных, сделав эту базу данных основной репликой в наборе реплик. Старые и новые шаблоны оформления синхронизируются, чтобы обновить изменения структуры. Чтобы этот код работал, необходимо создать основную реплику и реплику, включить их имена и пути, а затем запустить этот код из базы данных, отличной от старой или новой основной реплики.

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```

