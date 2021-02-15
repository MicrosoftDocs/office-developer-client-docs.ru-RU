---
title: Метод Open (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288401"
---
# <a name="open-method-ado-md"></a>Метод Open (ADO MD)

**Область применения**: Access 2013, Office 2013

Извлекает результаты многомерного запроса и возвращает результаты в ячейки.

## <a name="syntax"></a>Синтаксис

*Cellset*. Open *Source*, *ActiveConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Source* |Необязательный параметр. **Вариант,** который оценивает допустимый многомерный запрос, например запрос многомерных выражений (MDX). Аргумент *Source* соответствует свойству [Source.](source-property-ado-md.md) Дополнительные сведения о MDX см. в документации OLE DB for OLAP в microsoft Data Access Components SDK.|
|*ActiveConnection* |Необязательный параметр. Вариант, который оценивается в строку, указывав допустимую переменную объекта ADO [Connection или](connection-object-ado.md) определение для подключения.  Аргумент *ActiveConnection* указывает подключение, в котором необходимо открыть объект [Cellset.](cellset-object-ado-md.md) Если передать определение подключения для этого аргумента, ADO открывает новое подключение с использованием указанных параметров. Аргумент *ActiveConnection* соответствует свойству [ActiveConnection.](activeconnection-property-ado-md.md)|

## <a name="remarks"></a>Заметки

Метод **Open** создает ошибку, если один из его параметров опущен и соответствующее значение свойства не задано перед попыткой открыть **cellset.**

