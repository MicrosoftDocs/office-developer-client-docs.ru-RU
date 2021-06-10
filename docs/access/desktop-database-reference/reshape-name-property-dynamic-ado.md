---
title: Динамическое свойство Имя (ADO)
TOCTitle: Reshape Name dynamic property (ADO)
ms:assetid: 59ef99c8-da40-5cf6-b987-d47ea1433f45
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249307(v=office.15)
ms:contentKeyID: 48545030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b606960238e2f9a08d034ed92a79f7a767a1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306603"
---
# <a name="reshape-name-dynamic-property-ado"></a>Динамическое свойство Имя (ADO)


**Область применения**: Access 2013, Office 2013

Указывает имя объекта [Recordset.](recordset-object-ado.md)

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение **String,** которое является именем **Recordset.**

## <a name="remarks"></a>Примечания

Имена сохраняются в течение всего подключения или до закрытия **наборов** записей.

Свойство **Reshape Name** предназначено в основном для использования с функцией повторного формирования службы формирования данных Майкрософт для поставщика услуг [OLE DB.](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) Имена должны быть уникальными для того, чтобы участвовать в переоформлении.

Это свойство является только для чтения, но может быть установлено косвенно, когда создается Набор записей. Например, если предложение команды SHAPE создает набор recordset и дает ему псевдоним с ключевым словом "AS", то псевдоним назначен свойству Reshape Name. Если псевдоним не объявлен, свойством reshape name назначено уникальное имя, генерируемое службой формирования данных. Если имя псевдонима такое же, как и имя существующего **Recordset,** ни **Recordset** не будут переостановлены до тех пор, пока один из них не будет выпущен. Поведение по умолчанию можно изменить, задав свойство "Уникальные имена изменения" (см. свойство "Microsoft Data shaping service for OLE DB") для подключения ADO к TRUE. Это дает службе формирования данных разрешение на изменение имен пользователей в случае необходимости, чтобы застраховать уникальность.

Используйте свойство **Reshape Name,** если вы  хотите обратиться к набору записей в команде SHAPE или если вы не знаете его имя, так как оно было сгенерировано службой формирования данных. В этом случае можно создать команду SHAPE, сообразив команду вокруг строки, возвращаемой **свойством Reshape Name.**

**Reshape Name** — это динамическое свойство, применимое к коллекции [свойств](properties-collection-ado.md) объекта **Recordset,** когда свойство [CursorLocation](cursorlocation-property-ado.md) задано **для adUseClient.**

