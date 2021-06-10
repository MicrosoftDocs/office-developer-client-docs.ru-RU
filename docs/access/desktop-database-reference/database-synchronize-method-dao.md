---
title: Метод Database.Synchronize (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 411948f3c0ac4d6c353cd2722136dffb6a25fb17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294710"
---
# <a name="databasesynchronize-method-dao"></a>Метод Database.Synchronize (DAO)


**Область применения**: Access 2013, Office 2013

Синхронизирует две реплики. (Только для рабочих областей Microsoft Access.)

## <a name="syntax"></a>Синтаксис

*выражения* . Синхронизация ***(DbPathName***, ***ExchangeType***)

*выражение*: переменная, представляющая объект **Database**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Путь к целевой реплике, с которой будет синхронизирована база данных.</p></td>
</tr>
<tr class="even">
<td><p><em>ExchangeType</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong><a href="synchronizetypeenum-enumeration-dao.md">Константа SynchronizeTypeEnum,</a></strong> указывающая, в каком направлении синхронизировать изменения между двумя базами данных.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Синхронизация **используется для** обмена данными и изменения проектирования между двумя базами данных. Изменения в дизайне всегда происходят в первую очередь. Обе базы данных должны быть на одном уровне, прежде чем они смогут обмениваться данными. Например, обмен типом **dbRepExportChanges** может привести к изменениям в дизайне реплики, даже если изменения данных будут поступать только из базы данных в DbPathName.

Реплика, идентифицированная в DbPathName, должна быть частью одного и того же набора реплик. Если обе реплики имеют один и тот же параметр **свойства ReplicaID** или являются мастерами разработки для двух различных наборов реплик, синхронизация не удается.

При синхронизации двух реплик через Интернет необходимо использовать константу **dbRepSyncInternet.** В этом случае вместо указания локального сетевого пути необходимо указать адрес единого локатора ресурсов (URL-адрес) аргумента DbPathName.


> [!NOTE]
> Нельзя синхронизировать частичные реплики с другими частичными репликами. Дополнительные сведения см. в [методе PopulatePartial.](database-populatepartial-method-dao.md)


