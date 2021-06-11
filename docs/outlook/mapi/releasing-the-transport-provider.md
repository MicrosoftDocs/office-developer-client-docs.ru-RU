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

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Когда mapI или spooler MAPI заканчивается с помощью объекта транспортного логотипа:
  
1. MAPI или spooler MAPI вызывает метод [IXPLogon::TransportLogoff поставщика](ixplogon-transportlogoff.md) транспорта. 
    
2. Поставщик транспорта недействительный объект состояния вызывает [метод IMAPISupport::MakeInvalid.](imapisupport-makeinvalid.md) Является ли поставщик транспорта недействительными объекты сообщений, которые отправляются или получаются во время вызова **TransportLogoff,** зависит от флагов, переданных **в TransportLogoff.**
    
3. Поставщик транспорта вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объекта поддержки, чтобы удалить строку поставщика транспорта из таблицы состояния и удалить из внутренних таблиц все уникальные идентификаторы (UID), установленные с помощью метода [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md) Это ухитредит количество известных объектов с логотипом, активных на этом объекте поставщика. Если количество достигает нуля, MAPI вызывает [метод IXPProvider::Shutdown](ixpprovider-shutdown.md) и **release** на объекте поставщика. Если это был последний известный объект поставщика, использующий этот DLL в этом процессе, MAPI вызывает функцию **FreeLibrary** в DLL позже. Память для объекта поддержки MAPI освобождается, а метод выпуска **объектов** поддержки возвращается. 
    
4. Метод **TransportLogoff** возвращает S_OK. 
    
5. MAPI или spooler MAPI вызывает **release** на объекте logon поставщика транспорта. Память для объекта освобождена. 
    
6. MAPI или spooler MAPI вызывает **FreeLibrary** в поставщике DLL. 
    
Для надежности объекты logon и provider должны  иметь возможность самостоятельно обрабатывать окончательные вызовы выпуска без вызова их методов **TransportLogoff** или **Shutdown.** Если **выпуск** вызывается в таких случаях, транспортные поставщики должны относиться к вызовам так, как если **бы transportLogoff** или **Shutdown** были вызваны с нулевым аргументом, а затем **release**.
  

