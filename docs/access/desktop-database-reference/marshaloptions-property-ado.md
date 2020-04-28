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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289772"
---
# <a name="marshaloptions-property-ado"></a>Свойство MarshalOptions (ADO)


**Область применения**: Access 2013, Office 2013

Указывает, какие записи необходимо упаковать обратно на сервер.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [маршалоптионсенум](marshaloptionsenum.md) . Значение по умолчанию — **адмаршалалл**.

## <a name="remarks"></a>Примечания

При использовании [набора записей](recordset-object-ado.md)на стороне клиента записи, которые были изменены в клиенте, записываются обратно на средний уровень или на веб-сервер с помощью технологии, которая называется маршалингом, процесс упаковки и отправки параметров метода интерфейса для границ потоков или процессов. Установка свойства **MarshalOptions** может поспособствовать повышению производительности при маршалинге измененных удаленных данных для обратного обновления на среднем уровне или на веб-сервере.

**Использование удаленной службы данных** Это свойство используется только в **наборе записей**на стороне клиента.

