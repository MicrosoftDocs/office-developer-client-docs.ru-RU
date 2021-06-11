---
title: Каноническое свойство PidTagFolderWebViewInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316312"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>Каноническое свойство PidTagFolderWebViewInfo

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит URL-адрес домашней страницы папки в Microsoft Outlook. Это свойство содержит двоичный поток под названием **WebViewPersistenceObject.**
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Идентификатор:  <br/> |0x36DF  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Папка MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

URL-адрес домашней страницы может быть указан для любой Outlook папки. Эти сведения можно получить в Outlook на вкладке **Главная** страница диалогового окна Свойства для папки. 
  
В зависимости от определенных параметров политики главная страница может быть проигнорирована Outlook если магазин MAPI, содержащий эту папку, не сообщает MSCAP_SECURE_FOLDER_HOMEPAGES в реализации [IMSCapabilities::GetCapabilities.](pidtagfolderwebviewinfo-cannonical-property.md) 
  
И **папка Outlook Today,** и общедоступные папки могут иметь URL-адреса домашней страницы. Однако **папка Outlook Today** использует другой механизм для управления URL-адресом домашней страницы; этот механизм не охватывается в этом разделе. В общедоступных папках также может быть определен URL-адрес домашней страницы, который является специфическим для пользователя. Однако эта возможность не описана в этой теме. 
  
Значение этого свойства — двоичный поток, называемый **WebViewPersistenceObject.**
  
### <a name="webviewpersistenceobject-stream-structure"></a>Структура потока WebViewPersistenceObject

Структура **потока WebViewPersistenceObject** содержит сведения о URL-адресе домашней страницы для папки. 
  
Элементы данных в этой структуре хранятся в порядке маленького byte, сразу же следуя друг за другом в указанном ниже порядке. 
  
> [!NOTE]
> В следующем описании не может быть списка всех значений поля, поддерживаемых Outlook; Поэтому при считываемом кодом существующем потоке также могут быть найдены некоторые флаги, которые здесь не указаны. Однако это описание можно использовать для программного создания значений для свойства **PidTagFolderWebViewInfo,** которое Outlook понять. 
  
 _dwVersion_
  
> DWORD (4 bytes). Версия формата структуры. По Microsoft Office Outlook 2007 г. для этого поля поддерживается только одно значение.
    
|**Имя значения**|**Значение**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 bytes). Тип сведений о домашней странице. По Microsoft Office Outlook 2007 г. для этого поля поддерживается только одно значение.
    
|**Имя значения**|**Значение**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 bytes). Сочетание нулей или нескольких флагов, значения и значения которых перечислены в следующей таблице.
    
|Имя флага****|****Value** (Значение)**|****Описание****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |Главная **страница Show по** умолчанию для этого папки  была проверена на вкладке Главная страница диалоговое окно Свойства для папки.  <br/> |
   
 _dwUnused[7]_
  
> Массив из 7 элементов DWORD (всего 28 bytes). Неиспользовано.
    
cbData
  
> ULONG (4 bytes). Размер элемента  _данных wzURL_ в байтах. 
    
 _wzURL_
  
> Массив элементов WCHAR. Представление UTF-16 строки URL-адреса домашней страницы с нулевым прекращением.
    
### <a name="webviewpersistenceobject-stream-sample"></a>Образец потока WebViewPersistenceObject

В этом разделе описывается пример потока **WebViewPersistenceObject.** Поток указывает URL-адрес домашней страницы " https://www.microsoft.com ". 
  
 **Сброс данных**
  
Ниже приводится сброс данных потока, который будет отображаться в двоичном редакторе.
  
|**Смещение потока**|**Bytes data**|**Данные ASCII**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
Ниже приводится анализ примерных данных для **потока WebViewPersistenceObject.** 
  
 _dwVersion_
  
> Смещение 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Смещение 0x4, 4 байта: 0x00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Смещение 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused[7]_
  
> Смещение 0xC, 28 bytes: все нули.
    
 _cbData_
  
> Смещение 0x28, 4 bytes: 0x00000032.
    
 _wzURL_
  
> Смещение 0x2C, 0x32 байтов: массив из 25 WCHARs. Значение строки с нулевой строкой Unicode: https://www.microsoft.com ".
    

