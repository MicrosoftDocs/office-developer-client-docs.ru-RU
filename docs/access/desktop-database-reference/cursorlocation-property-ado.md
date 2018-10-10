---
title: CursorLocation Property (ADO)
TOCTitle: CursorLocation Property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9805b032a0e1a203d2a4057fb74757826a2a47b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481568"
---
# <a name="cursorlocation-property-ado"></a>CursorLocation Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает расположение службы курсора.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** , может быть установлено одно из значений [CursorLocationEnum](cursorlocationenum.md) .

## <a name="remarks"></a>Замечания

Это свойство можно выбрать одну из различных библиотек курсора, доступной для поставщика. Как правило вы можете выбрать одну с помощью библиотеки курсор на стороне клиента, либо, расположенного на сервере.

Установка этого свойства влияет только после установки свойства подключений. Изменение свойства **CursorLocation** не влияет на существующие подключения.

Курсоры, возвращенный методом [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) наследовать этот параметр. Объекты **набора записей** автоматически наследуют их связанного подключения этот параметр.

Это свойство является чтение и запись на [подключение](connection-object-ado.md) или закрытой [записей](recordset-object-ado.md)и только для чтения на открытие **набора записей**.

**Службы удаленных данных об использовании** При использовании на стороне клиента **записей** или объект **подключения** свойства **CursorLocation** может устанавливаться только для **adUseClient**.

