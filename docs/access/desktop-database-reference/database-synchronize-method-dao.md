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
ms.openlocfilehash: dc32087ad924a81eea5290d84ffb63dc4ad5e1ff
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999052"
---
# <a name="databasesynchronize-method-dao"></a>Метод Database.Synchronize (DAO)


**Применимо к**: Access 2013, Office 2013

Синхронизирует две реплики. (Microsoft Access рабочие области только).

## <a name="syntax"></a>Синтаксис

*выражение* . Синхронизация (***DbPathName***, ***ExchangeType***)

*выражение* Переменная, которая представляет собой объект **базы данных** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Путь к целевой реплики, с которой синхронизируется базы данных.</p></td>
</tr>
<tr class="even">
<td><p><em>ExchangeType</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> , которое указывает направление, чтобы синхронизировать изменения между двумя базами данных.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

**Синхронизация** использовать для обмена данными и разработки изменения между двумя базами данных. Изменение структуры всегда выполнять сначала. Обе базы данных должны быть на том же уровне структуры при обмене данными. Например обмен тип **dbRepExportChanges** может привести к изменения структуры в реплике несмотря на то, что изменения данных передаются только из базы данных для DbPathName.

Реплики, определенный в DbPathName необходимо быть членом один и тот же набор реплики. Если оба реплик иметь такое же значение свойства **ReplicaID** или реплик для двух различных наборов реплик, происходит сбой синхронизации.

При синхронизации двух реплик через Интернет, необходимо использовать **dbRepSyncInternet** константу. В этом случае укажите на универсальный код ресурса по URL-адрес для аргумента DbPathName вместо указания пути локальной сети.


> [!NOTE]
> Синхронизация частичных реплик с других частичных реплик. Метод [PopulatePartial](database-populatepartial-method-dao.md) для получения дополнительных сведений см.


