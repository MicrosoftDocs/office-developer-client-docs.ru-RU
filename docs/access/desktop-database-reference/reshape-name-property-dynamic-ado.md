---
title: Динамическое свойство Reshape Name (ADO)
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
# <a name="reshape-name-dynamic-property-ado"></a>Динамическое свойство Reshape Name (ADO)


**Область применения**: Access 2013, Office 2013

Указывает имя объекта [Recordset.](recordset-object-ado.md)

## <a name="return-values"></a>Возвращаемые значения

Возвращает **строку,** которая является именем **recordset.**

## <a name="remarks"></a>Заметки

Имена сохраняются в течение срока подключения или до закрытия **recordset.**

Свойство **Reshape Name** в основном предназначено для использования с функцией повторного формирования службы формирования данных [Майкрософт для поставщика службы OLE DB.](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) Имена должны быть уникальными для участия в повторном формировании.

Это свойство является только для чтения, но может быть установлено опосредованно при создания набора записей. Например, если предложение команды SHAPE создает набор записей и предоставляет ему псевдоним с ключевым словом "AS", то псевдоним назначен свойству Reshape Name. Если псевдоним не объявлен, свойству имени reshape будет назначено уникальное имя, которое создается службой формирования данных. Если имя псевдонима такое же, как и имя существующего наборов записей, ни **recordset** не будут повторно скомбинироваться до тех пор, пока один из них не будет отпущен. Поведение по умолчанию можно изменить, установив для свойства "Unique Reshape Names" (См. "Microsoft Data shaping service for OLE DB") в подключении ADO значение TRUE. Это дает службе формирования данных разрешение на изменение имен пользователей при необходимости для защиты уникальности.

Используйте свойство **Reshape Name,** если необходимо сослаться на объект **Recordset** в команде SHAPE или если вы не знаете его имя, так как оно было сгенерировано службой формирования данных. В этом случае можно создать команду SHAPE, совметив команду вокруг строки, возвращаемой свойством **Reshape Name.**

**Reshape Name** — это динамическое свойство, которое прикрепляется к коллекции [свойств](properties-collection-ado.md) объекта **Recordset,** когда свойству [CursorLocation](cursorlocation-property-ado.md) задано свойство **adUseClient.**

