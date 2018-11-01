---
title: Метод Reset (RDS - ссылки для настольных баз данных Access)
TOCTitle: Reset Method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab88aefabca73b9c2b23a4cf66664aa892310cdc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884487"
---
# <a name="reset-method-rds"></a>Метод Reset (RDS)


**Применимо к**: Access 2013, Office 2013

Выполняет сортировки или фильтрации со стороны клиента **набора записей** на основе указанного программная сортировка и фильтр свойств.

## <a name="syntax"></a>Синтаксис

*DataControl*. Reset (*значение*)

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

  - *value*

  - Необязательный параметр. **Логическое** значение, равное **True** (по умолчанию) Если требуется отфильтровать на текущем «отфильтрованные» строк. **Значение false** указывает, что фильтрации на исходной строк, удалить любые предыдущие параметры фильтра.

## <a name="remarks"></a>Замечания

[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента. Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца. Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше. Метод **Reset** будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.

При внесении изменений в исходных данных, который еще не был отправлен, метод **Сброс** завершится ошибкой. Во-первых используйте метод [SubmitChanges](submitchanges-method-rds.md) для сохранения изменений в чтение и запись **набора записей**, а затем **сбросить** метод для сортировки или фильтрации записей.

Если вы хотите выполнить более одного фильтра на набора строк, можно использовать необязательный аргумент *Boolean* с помощью метода **сбросить** . Следующем примере показано, как это сделать:

