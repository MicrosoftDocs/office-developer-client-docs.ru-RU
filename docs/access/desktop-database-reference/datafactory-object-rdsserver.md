---
title: Объект DataFactory (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4090b517dfdbe6d6870c04bf4118addad861ad95
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910637"
---
# <a name="datafactory-object-rdsserver"></a>Объект DataFactory (RDSServer)


**Применимо к**: Access 2013, Office 2013

Этот объект по умолчанию на сервере business реализует методы, обеспечивающие доступ к данным чтение и запись к источникам данных для клиентских приложений.

## <a name="remarks"></a>Примечания

Объект **RDSServer.DataFactory** разработан как объект автоматизации на сервере, которая принимает запросы клиентов. В реализацию Интернета он находится на веб-сервере и создается компонентом ADISAPI. Объект **RDSServer.DataFactory** предоставляет доступ на чтение и запись к источникам данных, но не содержит логику проверки или бизнес-правил.

При использовании метода, который доступен в **RDSServer.DataFactory** и [RDS. DataControl](datacontrol-object-rds.md) объекты удаленных данных служба использует **RDS. DataControl** версии по умолчанию. По умолчанию предполагается базового сценария программирования, где **RDSServer.DataFactory** выступает в качестве универсального на сервере бизнес-объект.

Если необходимо, чтобы веб-приложение для обработки задач обработки на сервере, можно заменить **RDSServer.DataFactory** пользовательский бизнес-объект.

Можно создать бизнес-сервере объекты, которые могут вызывать **RDSServer.DataFactory** методы, такие как [CreateRecordset](createrecordset-method-rds.md)и [запросов](query-method-rds.md) . Эта функция полезна, если вы хотите добавить функциональные возможности бизнес-объектов, но преимуществами существующих технологий удаленной службы данных.

Идентификатор класса для объекта **RDSServer.DataFactory** — 9381D8F5-0288-11 D 0-9501-00AA00B911A5.

