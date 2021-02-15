---
title: Объект DataFactory (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294479"
---
# <a name="datafactory-object-rdsserver"></a>Объект DataFactory (RDSServer)


**Область применения**: Access 2013, Office 2013

Этот бизнес-объект на стороне сервера по умолчанию реализует методы, которые предоставляют доступ на чтение и записи к указанным источникам данных для клиентских приложений.

## <a name="remarks"></a>Заметки

Объект **RDSServer.DataFactory** разработан как объект автоматизации на стороне сервера, который получает клиентские запросы. В реализации в Интернете он находится на веб-сервере и был созважен компонентом ADISAPI. Объект **RDSServer.DataFactory** предоставляет доступ на чтение и записи к указанным источникам данных, но не содержит логику проверки или бизнес-правил.

При использовании метода, доступного как в **RDSServer.DataFactory,** так и [в RDS. Объекты DataControl,](datacontrol-object-rds.md) служба удаленных данных использует **RDS. Версия DataControl** по умолчанию. По умолчанию предполагается базовый сценарий программирования, в котором **RDSServer.DataFactory** выступает в качестве универсального бизнес-объекта на стороне сервера.

Чтобы веб-приложение обрабатывал обработку на стороне сервера, можно **заменить RDSServer.DataFactory** пользовательским бизнес-объектом.

Можно создать серверные бизнес-объекты, которые вызовят методы **RDSServer.DataFactory,** такие как [Query](query-method-rds.md) и [CreateRecordset.](createrecordset-method-rds.md) Это полезно, если вы хотите добавить функциональные возможности в бизнес-объекты, но воспользоваться преимуществами существующих технологий удаленной службы данных.

ИД класса для объекта **RDSServer.DataFactory** — 9381D8F5-0288-11D0-9501-00AA00B911A5.

