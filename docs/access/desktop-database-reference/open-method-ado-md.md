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

Получает результаты многомерного запроса и возвращает результаты в набор ячеек.

## <a name="syntax"></a>Синтаксис

Набор *ячеек*. Открытый*источник*, *ActiveConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Source* |Необязательный атрибут. Значение **Variant** , которое оценивается как допустимый многомерный запрос, например многомерный запрос многомерных выражений (MDX). *Исходный* аргумент соответствует свойству [Source](source-property-ado-md.md) . Для получения дополнительных сведений об МНОГОМЕРных ВЫРАЖЕНИЯх обратитесь к документации по OLE DB для OLAP в пакете SDK компонентов MDAC Data Components.|
|*ActiveConnection* |Необязательный атрибут. Значение **Variant** , которое оценивается как строка, указывающая допустимое имя переменной объекта [подключения](connection-object-ado.md) ADO или определение подключения. Аргумент *ActiveConnection* указывает подключение, в котором будет открыт объект "набор [ячеек](cellset-object-ado-md.md) ". Если вы передаете определение подключения для этого аргумента, ADO открывает новое подключение, используя указанные параметры. Аргумент *ActiveConnection* соответствует свойству [ActiveConnection](activeconnection-property-ado-md.md) .|

## <a name="remarks"></a>Замечания

Метод **Open** создает ошибку, если какой-либо из его параметров опущен, а соответствующее значение свойства не было задано, прежде чем пытаться открыть набор **ячеек**.

