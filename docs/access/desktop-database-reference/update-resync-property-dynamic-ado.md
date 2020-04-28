---
title: Обновление динамического свойства Resync (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308346"
---
# <a name="update-resync-dynamic-property-ado"></a>Обновление динамического свойства Resync (ADO)


**Область применения**: Access 2013, Office 2013

Указывает, сопровождается ли метод [UpdateBatch](updatebatch-method-ado.md) неявным методом повторной [синхронизации](resync-method-ado.md) , и, если это так, областью этой операции.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает одно или несколько значений [перечисления адкпроп\_упдатересинк\_](adcprop-updateresync-enum.md) .

## <a name="remarks"></a>Примечания

Значения перечисления АДКПРОП\_упдатересинк\_могут сочетаться, за исключением адресинкалл, которые уже представляют сочетание остальных значений.

Константа **адресинкконфликтс** хранит значения повторной синхронизации в виде базовых значений, но не переопределяет ожидающие изменения.

**Повторная синхронизация обновлений** — это динамическое свойство, добавленное в [коллекцию свойств](properties-collection-ado.md) объекта [Recordset](recordset-object-ado.md) , если для свойства [CursorLocation](cursorlocation-property-ado.md) задано значение **адусеклиент**.

