---
title: TableDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4908699aaea69a001a1abd3761b78607ae2640a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869822"
---
# <a name="tabledefupdatable-property-dao"></a>TableDef.Updatable Property (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает значение, указывающее, является ли объект DAO можно изменить. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение* . Обновляемые

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

Настройка свойства **с возможностью записи** всегда является **True** для только что созданный объект **TableDef** и **значение False** для связанного объекта **TableDef** . Новый объект **TableDef** могут быть добавлены только базы данных, для которого у текущего пользователя есть разрешение на запись.

