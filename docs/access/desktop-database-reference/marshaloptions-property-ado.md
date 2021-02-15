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

Указывает, какие записи необходимо маршалировать обратно на сервер.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение [MarshalOptionsEnum.](marshaloptionsenum.md) Значение по умолчанию **— adMarshalAll.**

## <a name="remarks"></a>Заметки

При использовании клиентского [recordset](recordset-object-ado.md)записи, измененные на клиенте, записываюются обратно на средний уровень или веб-сервер с помощью метода маршалирования, процесса упаковки и отправки параметров метода интерфейса через границы потока или процесса. Установка свойства **MarshalOptions может** повысить производительность при маршализации измененных удаленных данных для обновления до среднего уровня или веб-сервера.

**Использование удаленной службы данных** Это свойство используется только в клиентском наборе **записей.**

