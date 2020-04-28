---
title: Метод Database. Synchronize (DAO)
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
# <a name="databasesynchronize-method-dao"></a>Метод Database. Synchronize (DAO)


**Область применения**: Access 2013, Office 2013

Синхронизирует две реплики. (Только для рабочих областей Microsoft Access.)

## <a name="syntax"></a>Синтаксис

*Expression* . Синхронизация (***дбпаснаме***, ***ексчанжетипе***)

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
<td><p><em>дбпаснаме</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Путь к целевой реплике, с которой будет синхронизироваться база данных.</p></td>
</tr>
<tr class="even">
<td><p><em>ексчанжетипе</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="synchronizetypeenum-enumeration-dao.md">синчронизетипинум</a></strong> , указывающая направление синхронизации изменений между двумя базами данных.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

**Синхронизация** используется для обмена данными и изменения структуры между двумя базами данных. Изменения макета всегда происходят первыми. Для обмена данными обе базы данных должны иметь одинаковый уровень оформления. Например, Exchange типа **дбрепекспортчанжес** может привести к изменениям структуры в реплике, несмотря на то, что изменения данных проходят только из базы данных в дбпаснаме.

Реплика, определенная в Дбпаснаме, должна быть частью того же набора реплик. Если обе реплики имеют одинаковое свойство **replicaId** или основные структуры для двух различных наборов реплик, синхронизация завершается с ошибкой.

При синхронизации двух реплик через Интернет необходимо использовать константу **дбрепсинЦинтернет** . В этом случае вместо указания пути к локальной сети необходимо указать URL-адрес для аргумента Дбпаснаме.


> [!NOTE]
> Невозможно синхронизировать частичные реплики с другими частичными репликами. Дополнительные сведения см. в методе [популатепартиал](database-populatepartial-method-dao.md) .


