---
title: MarshalOptions Property (ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482319"
---
# <a name="marshaloptions-property-ado"></a>MarshalOptions Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает, какие записи для маршалинга на сервере.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [MarshalOptionsEnum](marshaloptionsenum.md) . Значение по умолчанию — **adMarshalAll**.

## <a name="remarks"></a>Замечания

При использовании со стороны клиента [записей](recordset-object-ado.md), записи, которые были изменены в клиенте записываются на средний уровень или веб-сервер, называемый маршалинга, процесс упаковки и отправки параметров метода интерфейса через поток или границы процессов. Свойство **MarshalOptions** можно повысить производительность измененные удаленных данных — это упаковать для обновления в среднем уровне или в веб-сервере.

**Службы удаленных данных об использовании** Это свойство используется только на стороне клиента **набора записей**.

