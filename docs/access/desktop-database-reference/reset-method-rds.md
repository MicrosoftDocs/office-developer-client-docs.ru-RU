---
title: Метод Reset (RDS — справочник по базам данных Access для настольных пк)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306645"
---
# <a name="reset-method-rds"></a>Метод Reset (RDS)

**Область применения**: Access 2013, Office 2013

Выполняет сортировку или фильтрацию на клиентском наборе **записей** на основе указанных свойств сортировки и фильтра.

## <a name="syntax"></a>Синтаксис

*DataControl*. *Reset(value)*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*value* |Необязательный параметр. **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset. **False** означает, что вы фильтруете исходный набор строк, удаляя все предыдущие параметры фильтра.|

## <a name="remarks"></a>Заметки

Свойства [SortColumn,](sortcolumn-property-rds.md) [SortDirection,](sortdirection-property-rds.md) [FilterValue,](filtervalue-property-rds.md) [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) обеспечивают сортировку и фильтрацию в клиентском кэше. Функция сортировки заказывает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе критериев поиска, в то время как полный набор записей сохраняется в кэше. [](recordset-object-ado.md) Метод **Reset** выполнит условия и заменит текущий набор **recordset** на updatable **Recordset.**

При внесении изменений в исходные данные, которые еще не были отправлены, метод **сброса** не будет работать. Сначала используйте метод [SubmitChanges,](submitchanges-method-rds.md) чтобы сохранить все изменения в наборе записей для чтения и записи, а затем используйте метод **Reset** для сортировки или фильтрации записей.

Если вы хотите выполнить несколько фильтров в наборе строк, можно использовать необязательный *boolean* аргумент с методом **Reset.** В следующем примере показано, как это сделать.

