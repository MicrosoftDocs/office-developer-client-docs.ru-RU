---
title: Метод GetChildren (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292309"
---
# <a name="getchildren-method-ado"></a>Метод GetChildren (ADO)


**Область применения**: Access 2013, Office 2013


Возвращает набор [записей,](recordset-object-ado.md) строки которого представляют детей коллекции [Record](record-object-ado.md).

## <a name="syntax"></a>Синтаксис

**Установите** *запись набора*  =  *записей.* GetChildren

## <a name="return-value"></a>Возвращаемое значение

Объект **Recordset,** для которого каждая строка представляет собой дитя текущего объекта **Record.** Например, дети записи, представляют каталог, — это файлы и подтеки, содержащиеся в родительском каталоге. 

## <a name="remarks"></a>Примечания

Поставщик определяет, какие столбцы существуют в возвращаемом **наборе записей.** Например, поставщик источников документов всегда возвращает набор **записей ресурсов.**

