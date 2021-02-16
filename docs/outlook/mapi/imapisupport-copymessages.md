---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405158"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает сообщения из одной папки в другую.
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpSrcInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к папке, которая содержит сообщения для копирования или перемещений.
    
 _lpSrcFolder_
  
> [in] Указатель на папку, в которую будут скопированы или перемещены сообщения.
    
 _lpMsgList_
  
> [in] Указатель на массив идентификаторов записей, которые определяют сообщения для копирования или перемещений. 
    
 _lpDestInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к папке назначения для скопированные или перемещенные сообщения.
    
 _lpDestFolder_
  
> [in] Указатель на папку назначения для скопированные или перемещенные сообщения. Эта папка должна быть открыта.
    
 _ulUIParam_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI. Параметр _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в _ulFlags._
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI. Параметр _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в _ulFlags._
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет выполнением операции копирования или перемещения. Можно установить следующие флаги:
    
MESSAGE_DIALOG 
  
> Запрашивает отображение индикатора хода выполнения.
    
MESSAGE_MOVE 
  
> Сообщения должны быть перемещены, а не копироваться. Если MESSAGE_MOVE не установлен, сообщения копируется.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция копирования или перемещения прошла успешно.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::CopyMessages** реализован для объектов поддержки поставщика службы хранения сообщений. Поставщики store сообщений могут вызывать **IMAPISupport::CopyMessages** в своей реализации [IMAPIFolder::CopyMessages,](imapifolder-copymessages.md) чтобы скопировать или переместить одно или несколько сообщений из одной папки в другую. В рамках вызова **IMAPISupport::CopyMessages** поставщик store сообщений может указать, что MAPI должен отображать индикатор хода выполнения. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

