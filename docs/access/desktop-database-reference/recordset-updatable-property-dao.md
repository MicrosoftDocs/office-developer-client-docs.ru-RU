---
title: Recordset.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77f3c7331e42d0f9a63a0f87330f8acbc49a646b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480214"
---
# <a name="recordsetupdatable-property-dao"></a>Recordset.Updatable Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает значение, указывающее, является ли объект DAO можно изменить. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение* . Обновляемые

*выражение* Переменная, которая представляет собой объект **набора записей** .

## <a name="remarks"></a>Замечания

Моментальный снимок и прямого только – набора записей объекты типа всегда возвращает **значение False**.

Несколько типов объектов может содержать поля, которые не могут быть обновлены. Например можно создать объект типа динамического **набора записей** , в котором можно изменить только некоторые поля. Эти поля устранения или содержат данные, автоматически увеличивает или динамический набор может привести к из запроса, который объединяет обновляемых и nonupdatable таблицы.

Если объект содержит поля только для чтения, значение свойства **с возможностью записи** имеет **значение False**. Когда обновляемых одно или несколько полей, значение свойства — **True**. Можно изменить только обновляемых полей. Перехватываемые ошибка возникает при попытке присвоить новое значение в поле только для чтения.

Обновляемый объект может содержать поля только для чтения, перед изменить запись проверьте свойство **DataUpdatable** каждое поле в коллекции **полей** объекта **набора записей** .
