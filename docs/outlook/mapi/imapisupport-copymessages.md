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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _lpSrcInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к папке, которая содержит сообщения, которые будут скопированы или перемещены.
    
 _lpSrcFolder_
  
> [in] Указатель на папку, содержаную скопированные или перемещенные сообщения.
    
 _lpMsgList_
  
> [in] Указатель на массив идентификаторов записей, которые определяют сообщения, которые будут скопированы или перемещены. 
    
 _lpDestInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к папке назначения для скопированные или перенесенные сообщения.
    
 _lpDestFolder_
  
> [in] Указатель на папку назначения для скопированные или перенесенные сообщения. Эта папка должна быть открыта.
    
 _ulUIParam_
  
> [in] Указатель на объект progress, отображает индикатор прогресса. Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI. Параметр  _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в  _ulFlags_.
    
 _lpProgress_
  
> [in] Указатель на объект progress, отображает индикатор прогресса. Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI. Параметр  _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в  _ulFlags_.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют выполнение операции копирования или перемещения. Можно установить следующие флаги:
    
MESSAGE_DIALOG 
  
> Запрашивает отображение индикатора прогресса.
    
MESSAGE_MOVE 
  
> Сообщения должны быть перемещены, а не скопированы. Если MESSAGE_MOVE не установлено, сообщения копируется.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция копирования или перемещения была успешной.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::CopyMessages** реализован для объектов поддержки поставщиков сообщений. Поставщики магазинов сообщений могут вызывать **IMAPISupport::CopyMessages** при реализации [IMAPIFolder::CopyMessages,](imapifolder-copymessages.md) чтобы скопировать или переместить одно или несколько сообщений из одной папки в другую. В рамках вызова **IMAPISupport::CopyMessages** поставщик магазина сообщений может указать, что MAPI должен отображать индикатор прогресса. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

