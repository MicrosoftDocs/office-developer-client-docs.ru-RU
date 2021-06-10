---
title: Метод сброса (RDS - ссылка на настольные базы данных)
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
# <a name="reset-method-rds"></a>Метод сброса (RDS)

**Область применения**: Access 2013, Office 2013

Выполняет сортировку или фильтрацию на клиентском наборе **recordset** на основе указанных свойств сортировки и фильтрации.

## <a name="syntax"></a>Синтаксис

*DataControl*. Сброс *(значение*)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*value* |Необязательный параметр. Значение **Boolean** true **(по** умолчанию), если необходимо фильтровать текущий "фильтрованный" набор строк. **False** указывает, что вы фильтруете исходный набор строк, удаляя все предыдущие параметры фильтра.|

## <a name="remarks"></a>Примечания

Свойства [SortColumn,](sortcolumn-property-rds.md) [SortDirection,](sortdirection-property-rds.md) [FilterValue,](filtervalue-property-rds.md) [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) обеспечивают функции сортировки и фильтрации в клиентском кэше. Функция сортировки заказывает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе критериев поиска, а полный набор [записей](recordset-object-ado.md) поддерживается в кэше. Метод **Reset** выполнит критерии и заменит текущий **набор записей** на updatable **Recordset.**

Если будут внесены изменения в исходные данные, которые еще не были отправлены, метод **Сброса** не удастся. Сначала используйте метод [SubmitChanges](submitchanges-method-rds.md) для сохранения изменений в наборе записей чтения и записи, а затем используйте метод **Reset** для сортировки или фильтрации записей.

Если вы хотите выполнить несколько фильтров в строковом наборе, можно использовать необязательный аргумент *Boolean* с помощью метода **Reset.** В следующем примере показано, как это сделать.

