---
title: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f4bf93afc200edd88e89cf5d4e90435c2476942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313750"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a>Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)


**Область применения**: Access 2013, Office 2013

Позволяет внимательно контролировать изменения определенной базовой таблицы в наборе [записей,](recordset-object-ado.md) сформированном операцией JOIN на нескольких базовых таблицах.

  - **Уникальная** таблица указывает имя базовой таблицы, в которой разрешены обновления, вставки и удаления.

  - **Уникальная схема** указывает *схему* или имя владельца таблицы.

  - **Уникальный каталог** определяет *каталог или* имя базы данных, содержащей таблицу.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строку,** которая является именем таблицы, схемы или каталога.

## <a name="remarks"></a>Заметки

Желаемая базовая таблица уникально идентифицирована по каталогу, схеме и именам таблиц. При **наборе** свойства "Уникальная таблица" значения  свойств "Уникальная схема" или "Уникальный каталог" используются для поиска базовой таблицы.  Предполагается, но не обязательно, чтобы либо свойства **Unique Schema,** так и **Unique Catalog** были установлены до того, как будет установлено свойство **"Уникальная** таблица".

Первичный ключ **уникальной таблицы** рассматривается как первичный ключ всего **наборов записей.** Это ключ, используемый для любого метода, требующего первичного ключа.

Несмотря **на то что установлена** уникальная таблица, метод [Delete](delete-method-ado-recordset.md) влияет только на именоваемую таблицу. Методы [AddNew,](addnew-method-ado.md) [Resync,](resync-method-ado.md) [Update](update-method-ado.md)и [UpdateBatch](updatebatch-method-ado.md) влияют на все соответствующие базовые таблицы **recordset.**

**Уникальная** таблица должна быть указана перед любыми пользовательскими ресинхронизацией. Если **уникальная** таблица не указана, свойство [Resync Command](resync-command-property-dynamic-ado.md) не будет действовать.

Ошибка во время работы приводит к невозможности найти уникальную базовую таблицу.

Все эти динамические свойства appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.

