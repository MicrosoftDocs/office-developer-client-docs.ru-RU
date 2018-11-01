---
title: TableDef.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 9f38616a-41ee-cbd1-9e29-da436b258e08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198366(v=office.15)
ms:contentKeyID: 48546682
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f41433d90703f230e50f3248103777ec3aba325
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876458"
---
# <a name="tabledefvalidationtext-property-dao"></a>TableDef.ValidationText Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение **поля** объекта не удовлетворяют правило проверки, указанного идентификатором **условие на значение** свойства поля (только для рабочих областей Microsoft Access) . Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Сообщение об ошибке

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

Для объекта **[TableDef](tabledef-object-dao.md)** значение этого свойства доступно только для чтения для связанной таблицы, а также чтения и записи для базовой таблицы.

