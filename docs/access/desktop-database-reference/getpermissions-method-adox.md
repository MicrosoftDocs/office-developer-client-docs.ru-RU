---
title: Метод-Permissions (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa5dda3c8e2ee8251fc54f4ff3bc12be0aca5002
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292246"
---
# <a name="getpermissions-method-adox"></a>Метод-Permissions (ADOX)

**Область применения**: Access 2013, Office 2013

Возвращает разрешения для группы или пользователя в контейнере объекта или объекта.

## <a name="syntax"></a>Синтаксис

*ReturnValue* = *граупорусер*. При наличии полномочий (*Name*, *ObjectType* \[,*обжекттипеид*\])

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа Long** , задающее битовую маску, содержащую разрешения, которые группа или пользователь имеет для объекта. Это значение может быть одной или несколькими константами [ригхтсенум](rightsenum.md) .

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |Значение **Variant** , задающее имя объекта, для которого необходимо задать разрешения. Задайте для свойства *Name* значение null, если вы хотите получить разрешения для контейнера объектов.|
|*ObjectType* |**Длинное** значение, которое может быть одной из констант [обжекттипинум](objecttypeenum.md) , которое указывает тип объекта, для которого нужно получить разрешения.|
|*Обжекттипеид* |Необязательный атрибут. Значение **Variant** , задающее GUID для типа объекта поставщика, не определенного СПЕЦИФИКАЦИЕЙ OLE DB. Этот параметр является обязательным, если параметр *ObjectType* имеет значение **адпермобжпровидерспеЦифик**; в противном случае он не используется.|

