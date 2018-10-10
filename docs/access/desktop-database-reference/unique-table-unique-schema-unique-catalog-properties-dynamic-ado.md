---
title: Unique Table, Unique Schema, Unique Catalog Properties--Dynamic (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog Properties--Dynamic (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd21c8b7c71f5fe1c95d347758e486f3854efab0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480475"
---
# <a name="unique-table-unique-schema-unique-catalog-properties--dynamic-ado"></a>Unique Table, Unique Schema, Unique Catalog Properties--Dynamic (ADO)


**Применимо к**: Access 2013 | Office 2013

Позволяет тесно управления изменения определенного базовые таблицы в [набор записей](recordset-object-ado.md) , которая была создана с помощью операции ОБЪЕДИНЕНИЯ на нескольких базовых таблиц.

  - **Уникальная таблица** указывает имя базовая таблица после обновления, вставки и удаления, разрешены.

  - **Уникальный схемы** указывает *схемы*или имя владельца таблицы.

  - **Уникальный каталог** указывает *каталог*или имя базы данных, содержащий таблицу.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **String** , — это имя таблицы, схемы или каталога.

## <a name="remarks"></a>Замечания

Требуемое базовая таблица однозначно определяется его каталога, схемы и имена таблиц. Если свойство **Уникальной таблицы** , значения свойств **Уникальный схемы** и **Уникальные каталогов** используются для поиска базовая таблица. Он предназначен, но не требуется, что один или оба свойства **Уникальный схемы** и **Уникальные каталога** задать перед свойству **Уникальной таблицы** .

Первичный ключ в **Таблице уникальный** обрабатывается как первичный ключ всего **набора записей**. Это ключ, используемый для любого метода, требующие первичный ключ.

Во время **Уникальной таблицы** имеет значение, метод [Delete](delete-method-ado-recordset.md) действует только именованные таблицу. Методы [AddNew](addnew-method-ado.md), [выполнить повторную синхронизацию](resync-method-ado.md), [обновления](update-method-ado.md)и [UpdateBatch](updatebatch-method-ado.md) влияет на все соответствующие базовые таблицы из **набора записей**.

Перед выполнением любого настраиваемого нарушением должен быть указан **Уникальной таблицы** . Если **Уникальной таблицы** не указан, [Команда выполнить повторную синхронизацию](resync-command-property-dynamic-ado.md) свойство не будет действовать.

Если не удается найти уникальный базовая таблица приводит к ошибке времени выполнения.

Эти динамические свойства всех присоединяются к коллекции [свойств](properties-collection-ado.md) объекта **набора записей** при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.

