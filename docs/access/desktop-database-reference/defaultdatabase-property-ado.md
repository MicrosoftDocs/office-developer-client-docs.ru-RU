---
title: Свойство DefaultDatabase (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 01ca42ff738afe3a35cab6263cdae32ac256f3d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702644"
---
# <a name="defaultdatabase-property-ado"></a>Свойство DefaultDatabase (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает базу данных по умолчанию для объекта [подключения](connection-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, которое оценивается как имя базы данных, доступные из поставщика.

## <a name="remarks"></a>Замечания

Свойство **DefaultDatabase** задает или возвращает имя базы данных по умолчанию для определенного объекта **подключения** .

Если база данных по умолчанию, строк SQL использовать значение без указания единицы синтаксис для доступа к объектам в этой базе данных. Для доступа к объектам в базу данных, указанных в свойстве **DefaultDatabase** , необходимо указать имена объектов с именем нужной базы данных. При подключении поставщика запишет сведения о базе данных по умолчанию для свойства **DefaultDatabase** . Некоторые поставщики разрешить подключения только одна база данных, в этом случае не может изменить свойство **DefaultDatabase** .

Некоторые источники данных и поставщики могут не поддерживать этот компонент и может возвращать сообщение об ошибке или пустая строка.

**Службы удаленных данных об использовании** Это свойство недоступно на объект **подключения** со стороны клиента.

