---
title: Supports Method (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceeab22cda05738fdcec090acb5b4a2d6fc88a5b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604262"
---
# <a name="supports-method-ado"></a>Supports Method (ADO)


**Применимо к**: Access 2013 | Office 2013

Определяет, поддерживает ли указанный объект [набора записей](recordset-object-ado.md) определенного типа функциональные возможности.

## <a name="syntax"></a>Синтаксис

*Логическое* = *набора записей*. Поддерживает (*CursorOptions*)

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Возвращает **логическое** значение, указывающее, поддерживается ли все компоненты, определяемого аргументом *CursorOptions* поставщиком.

## <a name="parameters"></a>Параметры

  - *CursorOptions*

  - **Длинное** выражение, которое состоит из одного или нескольких значений [CursorOptionEnum](cursoroptionenum.md) .

## <a name="remarks"></a>Замечания

Используйте метод **поддерживает** , чтобы определить, какие функциональные возможности поддерживает объект **набора записей** . Если объект **набора записей** не поддерживают возможности, соответствующий константы находятся в *CursorOptions*, метод **поддерживает** возвращает **значение True**. В противном случае возвращает **значение False**.


> [!NOTE]
> <P>Несмотря на то, что метод <STRONG>поддерживает</STRONG> может возвращать <STRONG>значение True</STRONG> для указанной функции, не гарантирует, что поставщик можно включить ни при каких обстоятельствах. Метод <STRONG>поддерживает</STRONG> просто возвращает поставщик поддерживает ли эта функция, при условии определенных условий. Например метод <STRONG>поддерживает</STRONG> может указывать, что объект <STRONG>набора записей</STRONG> поддерживает обновления, даже если курсор основан на нескольких присоединиться к таблице, некоторые столбцы, не обновляются.</P>


