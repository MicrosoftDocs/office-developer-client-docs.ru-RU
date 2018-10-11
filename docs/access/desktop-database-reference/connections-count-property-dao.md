---
title: Connections.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4f341abfea455acdc96a2883d0f4dee3bd2a5fe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480509"
---
# <a name="connectionscount-property-dao"></a>Connections.Count Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает количество объектов **[подключения](connection-object-dao.md)** в коллекции **[подключений](connections-collection-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . Count

*выражение* Переменная, которая представляет собой объект- **подключений** .

## <a name="remarks"></a>Замечания

Так как члены коллекции начинаются с 0, должны всегда кода циклов, начиная с элемента 0 и заканчивая значение свойства **Count** минус 1. Если вы хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , можно использовать **For Each... Далее** команды.

Значение свойства **Count** никогда не имеет значение Null. Если значение равно 0, нет объектов в коллекции.

