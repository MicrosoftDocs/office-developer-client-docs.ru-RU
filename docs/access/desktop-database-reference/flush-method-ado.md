---
title: Flush Method - ActiveX Data Objects (ADO)
TOCTitle: Flush method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a55eb66c454d510d53083c495326548eda08af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292344"
---
# <a name="flush-method-ado"></a>Метод Flush (ADO)


**Область применения**: Access 2013, Office 2013

Привнося содержимое потока, [оставшегося](stream-object-ado.md) в буфере ADO, к основному объекту, с которым связан **Stream.**

## <a name="syntax"></a>Синтаксис

*Stream*. Flush

## <a name="remarks"></a>Заметки

Этот метод можно использовать для отправки содержимого буфера потоков в объект, на который он основан (например, узел или файл, представленный URL-адресом, который является источником объекта **Stream).** Этот метод следует использовать, чтобы убедиться, что все изменения, внесенные в содержимое **stream,** были записаны. Однако в ADO обычно не требуется вызывать очистку, так как ADO постоянно очищает буфер как можно больше в фоновом режиме. Изменения содержимого **stream** внося автоматически, а не кэшируются до тех пор, пока не будет **вызвана** очистка.

Закрытие потока **с** помощью метода [Close](close-method-ado.md) автоматически очищает содержимое **потока;** Нет необходимости явным образом вызывать очистку **непосредственно** **перед** close.

