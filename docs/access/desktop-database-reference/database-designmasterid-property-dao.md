---
title: Свойство Database.DesignMasterID (DAO)
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
# <a name="databasedesignmasterid-property-dao"></a>Свойство Database.DesignMasterID (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение 16-byte, которое уникально определяет мастер дизайна в наборе реплик (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . DesignMasterID

*выражение*: переменная, представляющая объект **Database**.

## <a name="remarks"></a>Примечания

Свойство **DesignMasterID следует** задать только в том случае, если необходимо переместить текущий мастер дизайна. При настройке этого свойства создается определенная реплика в реплике, заданной мастером разработки.

> [!NOTE]
> Никогда не создайте второго мастера дизайна в наборе реплик. Существование второго мастера разработки может привести к потере данных.

В экстремальных условиях, например, если мастер дизайна стерт или поврежден, вы можете установить это свойство в текущей реплике. Однако установка этого свойства на реплику, когда в наборе уже есть другой мастер разработки, может привести к разделению реплики на два непримиримых набора и предотвратить дальнейшую синхронизацию данных.

Если вы решите сделать реплику нового мастера дизайна для набора, синхронизуй ее со всеми репликами в наборе реплик перед установкой свойства **DesignMasterID** в реплике. Реплика должна быть открыта в эксклюзивном режиме, чтобы сделать ее мастером дизайна.

Если вы сделаете реплику, назначенную только для чтения в мастере разработки, то целевая реплика будет выполнена для чтения и записи; старый мастер дизайна также остается чтением и написанием.

Параметр **свойства DesignMasterID** хранится в таблице системы MSysRepInfo.

## <a name="example"></a>Пример

В этом примере свойство **DesignMasterID** задает параметр **свойства ReplicaID** другой базы данных, что делает эту базу данных мастером разработки в наборе реплик. Старые и новые мастера дизайна синхронизируются для обновления изменения дизайна. Чтобы этот код работал, необходимо создать мастер дизайна и реплику, включить их имена и пути по мере необходимости и запустить этот код из базы данных, кроме старого или нового мастера разработки.

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

