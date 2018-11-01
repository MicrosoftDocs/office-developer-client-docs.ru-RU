---
title: Отправка команд базовому поставщику данных
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0379d38b6c38145a72d5ab41b7ee0e7ec45531b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889079"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Отправка команд базовому поставщику данных


**Применимо к**: Access 2013, Office 2013

Любые команды, не начинается с ФИГУРЫ передается через поставщика данных. Это эквивалентно команды фигуры в форме «ФИГУРЫ {поставщика команды}». Выполните эти команды *не* имеет для создания **записей**. Для экземпляра «ФИГУРЫ {РАЗМЕЩЕНИЯ ТАБЛИЦУ MyTable} — это команда действителен фигуры, при условии, что поставщик данных поддерживает размещения сообщений в ТАБЛИЦЕ.

Эта возможность позволяет как обычный поставщика команды и фигуры для совместного использования одного подключения и транзакций.

