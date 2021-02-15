---
title: Метод GetPermissions (ADOX)
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
# <a name="getpermissions-method-adox"></a>Метод GetPermissions (ADOX)

**Область применения**: Access 2013, Office 2013

Возвращает разрешения для группы или пользователя в объекте или контейнере объектов.

## <a name="syntax"></a>Синтаксис

*ReturnValue*  =  *GroupOrUser*. GetPermissions(*Name*, *ObjectType* \[ ,*ObjectTypeId* \] )

## <a name="return-value"></a>Возвращаемое значение

Возвращает **длинное значение,** которое указывает битовуюmask, содержащую разрешения, которые есть у группы или пользователя в объекте. Это значение может быть одной или более из [констант RightsEnum.](rightsenum.md)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |Значение **Variant,** которое указывает имя объекта, для которого необходимо установить разрешения. Установите *для name* значение null, если вы хотите получить разрешения для контейнера объектов.|
|*ObjectType* |Длинное значение, которое может быть одной из [констант ObjectTypeEnum,](objecttypeenum.md) которое указывает тип объекта, для которого необходимо получить разрешения. |
|*ObjectTypeId* |Необязательный параметр. Значение **Variant,** которое указывает GUID для типа объекта поставщика, не определенного спецификацией OLE DB. Этот параметр обязален, если *для ObjectType* задан параметр **adPermObjProviderSpecific;** в противном случае он не используется.|

