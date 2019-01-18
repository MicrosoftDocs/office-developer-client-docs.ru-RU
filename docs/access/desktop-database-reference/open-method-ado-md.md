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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703834"
---
# <a name="open-method-ado-md"></a>Метод Open (ADO MD)

**Применимо к**: Access 2013, Office 2013

Получает результаты запроса многомерных и возвращает результаты для набора ячеек.

## <a name="syntax"></a>Синтаксис

*Набор ячеек*. Откройте*исходный*, *ActiveConnection*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Source* |Необязательно. **Variant** , которое оценивается как допустимый запрос многомерных, например запрос многомерных выражений (MDX). *Исходный* аргумент соответствует свойство [Source](source-property-ado-md.md) . Дополнительные сведения о многомерных Выражений можно OLE DB для OLAP документация в пакете SDK компонентов доступа к данным Microsoft.|
|*ActiveConnection* |Необязательно. **Variant** , которое оценивается как строка, задающая допустимое имя переменной объекта ADO- [подключение](connection-object-ado.md) или определения для подключения. Аргумент *ActiveConnection* указывает подключения для открытия объекта [ячеек](cellset-object-ado-md.md) . Если передать определение подключения для этого аргумента ADO откроется новое подключение с помощью указанных параметров. Аргумент *ActiveConnection* соответствует свойству [ActiveConnection](activeconnection-property-ado-md.md) .|

## <a name="remarks"></a>Замечания

Метод **Open** приводит к ошибке, если один из его параметров указан и перед попыткой открыть **ячеек**не задано значение его соответствующего свойства.

