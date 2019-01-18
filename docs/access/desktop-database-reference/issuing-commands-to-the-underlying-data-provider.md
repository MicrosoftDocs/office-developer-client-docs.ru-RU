---
title: Отправка команд базовому поставщику данных
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709616"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Отправка команд базовому поставщику данных

**Применимо к**: Access 2013, Office 2013

Любые команды, не начинается с ФИГУРЫ передается через поставщика данных. Это эквивалентно команды фигуры в форме «ФИГУРЫ {поставщика команды}». Выполните эти команды *не* имеет для создания **записей**. Для экземпляра «ФИГУРЫ {РАЗМЕЩЕНИЯ ТАБЛИЦУ MyTable} — это команда действителен фигуры, при условии, что поставщик данных поддерживает размещения сообщений в ТАБЛИЦЕ.

Эта возможность позволяет как обычный поставщика команды и фигуры для совместного использования одного подключения и транзакций.

