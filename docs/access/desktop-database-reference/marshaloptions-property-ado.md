---
title: Свойство MarshalOptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704597"
---
# <a name="marshaloptions-property-ado"></a>Свойство MarshalOptions (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает, какие записи для маршалинга на сервере.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [MarshalOptionsEnum](marshaloptionsenum.md) . Значение по умолчанию — **adMarshalAll**.

## <a name="remarks"></a>Замечания

При использовании со стороны клиента [записей](recordset-object-ado.md), записи, которые были изменены в клиенте записываются на средний уровень или веб-сервер, называемый маршалинга, процесс упаковки и отправки параметров метода интерфейса через поток или границы процессов. Свойство **MarshalOptions** можно повысить производительность измененные удаленных данных — это упаковать для обновления в среднем уровне или в веб-сервере.

**Службы удаленных данных об использовании** Это свойство используется только на стороне клиента **набора записей**.

