---
title: Свойство RecordCount (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5ab01c419f703c1c17b1bf2b2cca2fb3844655d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300772"
---
# <a name="recordcount-property-ado"></a>Свойство RecordCount (ADO)


**Область применения**: Access 2013, Office 2013

Указывает количество записей в [объекте Recordset.](recordset-object-ado.md)

## <a name="return-value"></a>Возвращаемое значение

Возвращает **длинное** значение, которое указывает количество записей в **наборе записей.**

## <a name="remarks"></a>Заметки

Используйте свойство **RecordCount,** чтобы узнать, сколько записей находится в **объекте Recordset.** Свойство возвращает -1, если ADO не может определить количество записей или если поставщик или тип курсора не поддерживает **RecordCount.** Чтение свойства **RecordCount** в закрытом наборе **записей** приводит к ошибке.

Если объект **Recordset** поддерживает приблизительное расположение или закладки , то есть **Supports (adApproxPosition)** или **Supports (adBookmark)** соответственно, возвращает **значение True,** это значение будет точным числом записей в наборе **записей** независимо от того, было ли оно полностью заполнено. Если объект **Recordset** не поддерживает приблизительное позиционирование, это свойство может быть значительным ресурсоемким, так как для возврата точного значения **RecordCount** необходимо извлечь и подсчитать все записи.

Тип курсора объекта **Recordset** влияет на то, можно ли определить число записей. Свойство **RecordCount** возвращает -1 для курсора только вперед; фактическое число для курсора статического или наборов ключей; и -1 или фактическое число динамических курсоров в зависимости от источника данных.

