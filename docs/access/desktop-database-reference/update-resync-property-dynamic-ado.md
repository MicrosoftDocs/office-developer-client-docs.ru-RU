---
title: Обновление свойства динамического повторной синхронизации (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702028"
---
# <a name="update-resync-dynamic-property-ado"></a>Обновление свойства динамического повторной синхронизации (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает, будет ли метод [UpdateBatch](updatebatch-method-ado.md) следуют неявных [выполнить повторную синхронизацию](resync-method-ado.md) метод операцию и если да, области действия этой операции.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает один или несколько [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) значения.

## <a name="remarks"></a>Замечания

Значения ADCPROP\_UPDATERESYNC\_ENUM может быть объединен, за исключением adResyncAll, который уже представляет сочетание остальные значения.

Константы **adResyncConflicts** хранятся значения повторной синхронизации как базового значения, но не переопределяет ожидающих изменений.

**Обновление выполнить повторную синхронизацию** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта [набора записей](recordset-object-ado.md) при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.

