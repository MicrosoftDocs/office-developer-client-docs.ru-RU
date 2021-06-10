---
title: Метод SetPermissions (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314583"
---
# <a name="setpermissions-method-adox"></a>Метод SetPermissions (ADOX)

**Область применения**: Access 2013, Office 2013

Указывает разрешения для группы или пользователя объекта.

## <a name="syntax"></a>Синтаксис

*GroupOrUser*. SetPermissions *Name,* *ObjectType*, *Action*, *Rights* \[ ,*Inherit* \] \[ ,*ObjectTypeId*\]

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Name* |Значение **String,** которое указывает имя объекта, для которого необходимо установить разрешения.|
|*ObjectType* |**Длинное** значение, которое может быть одной из констант [ObjectTypeEnum,](objecttypeenum.md) которое указывает тип объекта, для которого необходимо получить разрешения.|
|*Действие* |**Длинное** значение, которое может быть одним из констант [ActionEnum,](actionenum.md) которое указывает тип действий, выполняемых при установке разрешений.|
|*Rights* |**Длинное** значение, которое может быть битом одной или более констант [RightsEnum,](rightsenum.md) которое указывает права на набор.|
|*Наследование* |Необязательный параметр. **Длинное** значение, которое может быть одним из [констант InheritTypeEnum,](inherittypeenum.md) которое указывает, как объекты будут наследовать эти разрешения. По умолчанию значение **adInheritNone**.|
|*ObjectTypeId* |Необязательный параметр. Значение **Variant,** которое указывает GUID для типа объекта поставщика, не определенного спецификацией OLE DB. Этот параметр необходим, если *objectType* задан **в adPermObjProviderSpecific;** в противном случае он не используется.|

## <a name="remarks"></a>Примечания

Ошибка произойдет, если поставщик не поддерживает установку прав доступа для групп или пользователей.

> [!NOTE]
> При **вызове SetPermissions** настройка **Действия для adAccessRevoke** переопределяет все параметры *параметра Rights.* Не *задайте действия* **adAccessRevoke,** если вы хотите, чтобы права, указанные в параметре *Rights,* вступили в силу.


