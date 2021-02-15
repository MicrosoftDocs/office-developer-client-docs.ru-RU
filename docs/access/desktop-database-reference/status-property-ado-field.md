---
title: Свойство Status (Field в ADO)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9c5f9d73a1081bb27c88541ac99307165222ab65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306323"
---
# <a name="status-property-ado-field"></a>Свойство Status (Field в ADO)


**Область применения**: Access 2013, Office 2013

Указывает состояние объекта [Field.](field-object-ado.md)

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [FieldStatusEnum.](fieldstatusenum.md) Значение по умолчанию **— adFieldOK.**

## <a name="remarks"></a>Заметки

Это свойство всегда возвращает **adFieldOK для** полей объекта [Recordset.](recordset-object-ado.md)

Добавления и удаления в коллекции [Fields](fields-collection-ado.md) объекта [Record](record-object-ado.md) кэшются до тех пор, пока не будет вызван метод [Update.](update-method-ado.md) Свойство **Status** позволяет определить, какие поля были успешно добавлены или удалены.

Для повышения производительности изменения схемы  кэшются до тех пор, пока не будет вызвано обновление, а затем изменения будут внесены в пакетное оптимистичное обновление. Если метод **Update** не вызван, сервер не обновляется. Если какие-либо обновления не будут обновлены, возвращается ошибка, а свойство **Status** указывает объединенные значения кода состояния операции и ошибки. Например, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**. Свойство **Status** для каждого **поля** можно использовать, чтобы определить, почему поле не было добавлено, изменено или удалено.  **Состояние** только осмысленно фиксироваться в **записи.** **Коллекция Fields,** а не **Recordset.** **Коллекция Fields.**

При добавлении, изменении или удалении поля могут возникнуть две **проблемы.** Если пользователь удаляет **поле,** оно помечается для удаления из коллекции **Fields.** Если последующее обновление возвращает ошибку, так  как пользователь попытался удалить поле, для которого у них нет разрешения, поле будет иметь состояние **adFieldPermissionDenied** **OR**  **adFieldPendingDelete**.  При [вызове метода CancelUpdate](cancelupdate-method-ado.md) восстанавливаются исходные значения и **устанавливается** состояние **adFieldOK.** Аналогичным образом метод **Update** может возвращать ошибку, так как было добавлено новое **поле** и ему было задано недопустимое значение. В этом случае  новое поле будет в коллекции **Fields** и будет иметь состояние **adFieldPendingInsert** и, **возможно, adFieldCantCreate.** Вы можете увести соответствующее значение для нового **поля и** снова вызвать **update.** Обратите внимание, что вызов **Resync** вместо этого повторно вызывает поставщика.

