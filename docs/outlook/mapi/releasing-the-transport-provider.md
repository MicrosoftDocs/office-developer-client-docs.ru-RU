---
title: Освобождение поставщика транспорта
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328387"
---
# <a name="releasing-the-transport-provider"></a>Освобождение поставщика транспорта

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Когда MAPI или пулер MAPI завершит работу с объектом для переноса для логотипа:
  
1. MAPI или пулер MAPI вызывает метод [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) поставщика транспорта. 
    
2. Поставщик транспорта аннулирует объект состояния, вызывая метод [IMAPISupport::MakeInvalid.](imapisupport-makeinvalid.md) То, делает ли поставщик транспорта недопустимыми объекты сообщений, которые отправляются или получаются во время вызова **TransportLogoff,** зависит от флагов, переданных **в TransportLogoff.**
    
3. Поставщик транспорта вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объекта поддержки, чтобы удалить строку поставщика транспорта из таблицы состояния и удалить из внутренних таблиц все уникальные идентификаторы (UID), которые были установлены с помощью метода [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md) Он многчит количество активных известных объектов для работы с сайтом поставщика. Если количество достигает нуля, MAPI вызывает метод [IXPProvider::Shutdown](ixpprovider-shutdown.md) и **Release** для объекта поставщика. Если это был последний известный объект поставщика, использующий эту DLL в этом процессе, MAPI вызывает функцию **FreeLibrary** для DLL позже. Память для объекта поддержки MAPI освобождается, и возвращается метод **release** объекта поддержки. 
    
4. Метод **TransportLogoff** возвращает S_OK. 
    
5. MAPI или пулер MAPI вызывает **release** для объекта для эмблемы поставщика транспорта. Память для объекта отпущена. 
    
6. MAPI или пулер MAPI вызывает **FreeLibrary** в DLL поставщика. 
    
Для обеспечения надежности объекты для выхода и  поставщиков должны иметь возможность обрабатывать окончательные вызовы выпуска для себя без вызова методов **TransportLogoff** или **Shutdown.** Если **в** таких случаях вызывается выпуск, поставщики транспорта должны рассматривать вызовы так, как если бы **вызовы TransportLogoff** или **Shutdown** были вызваны с аргументом "ноль", за которым следует **release**.
  

