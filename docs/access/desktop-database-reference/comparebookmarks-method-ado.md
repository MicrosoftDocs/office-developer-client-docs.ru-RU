---
title: Метод CompareBookmarks (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 460a77284141daad1834699c4dc1775be05c5c26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296096"
---
# <a name="comparebookmarks-method-ado"></a>Метод CompareBookmarks (ADO)

**Область применения**: Access 2013, Office 2013

Сравнивает две закладки и возвращает индикатор их относительных значений.

## <a name="syntax"></a>Синтаксис

*result*  =  *recordset*. CompareBookmarks(*Bookmark1*, *Bookmark2*)

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [CompareEnum,](compareenum.md) которое указывает относительное положение строки двух записей, представленных закладки.

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Bookmark1* |Закладка первой строки.|
|*Bookmark2* |Закладка второй строки.|

## <a name="remarks"></a>Заметки

Закладки должны применяться к одному объекту [Recordset](recordset-object-ado.md) или **объекту Recordset** и его [клону.](clone-method-ado.md) Невозможно надежно сравнить закладки из разных объектов **Recordset,** даже если они были созданы из одного источника или команды. Также нельзя сравнить закладки для объекта **Recordset,** чей поставщик не поддерживает сравнения.

Закладка уникально идентифицирует строку в **объекте Recordset.** Используйте свойство [bookmark](bookmark-property-ado.md) текущей строки для получения закладки.

Так как тип данных закладки является конкретным поставщиком, ADO предоставляет его как вариант. Например, SQL Server закладки имеют тип DBTYPE \_ R8 (Double). ADO предоставляет этот тип как Variant с подтипом Double.

При сравнении закладок ADO не пытается привести какой-либо тип. Значения просто передаются поставщику, где происходит сравнение. Если закладки, переданные методу **CompareBookmarks,** хранятся в переменных различных типов, это может привести к ошибке несоответствия типа" "Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом".

Недостоверная или неправильно сформированная закладка приведет к ошибке.

