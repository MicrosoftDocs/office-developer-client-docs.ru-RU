---
title: Свойство MarshalOptions (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5983b7794677b5cc584c541289069acf282d9f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883213"
---
# <a name="marshaloptions-property-ado"></a>Свойство MarshalOptions (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает, какие записи для маршалинга на сервере.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [MarshalOptionsEnum](marshaloptionsenum.md) . Значение по умолчанию — **adMarshalAll**.

## <a name="remarks"></a>Замечания

При использовании со стороны клиента [записей](recordset-object-ado.md), записи, которые были изменены в клиенте записываются на средний уровень или веб-сервер, называемый маршалинга, процесс упаковки и отправки параметров метода интерфейса через поток или границы процессов. Свойство **MarshalOptions** можно повысить производительность измененные удаленных данных — это упаковать для обновления в среднем уровне или в веб-сервере.

**Службы удаленных данных об использовании** Это свойство используется только на стороне клиента **набора записей**.

