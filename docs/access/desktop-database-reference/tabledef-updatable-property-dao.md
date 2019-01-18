---
title: Свойство TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725975"
---
# <a name="tabledefupdatable-property-dao"></a>Свойство TableDef.Updatable (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает значение, указывающее, является ли объект DAO можно изменить. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение* . Обновляемые

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

Настройка свойства **с возможностью записи** всегда является **True** для только что созданный объект **TableDef** и **значение False** для связанного объекта **TableDef** . Новый объект **TableDef** могут быть добавлены только базы данных, для которого у текущего пользователя есть разрешение на запись.

