---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2ed71b5eef0c25a78d7c8ec695a756a02e796dbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586034"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Откроется интерфейс [IMAPIFormMgr](imapiformmgriunknown.md) на объект поставщика библиотеки форм в контексте существующего сеанса. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>Параметры

 _pSession_
  
> [in] Указатель на сеанс используется клиентским приложением.
    
 _ppmgr_
  
> [out] Указатель на возвращенный интерфейс **IMAPIFormMgr** . 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

После клиентское приложение вызывает функцию **MAPIOpenFormMgr** , большинство последующих связанных с forms происходят взаимодействия через поставщика библиотеки форм или интерфейс, возвращенные поставщиком библиотеки форм. Интерфейс **IMAPIFormMgr** позволяет клиента для работы с обработчики сообщений и выполнять с разрешением от классов сообщений и библиотеки форм. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp Откроется диспетчер форм, можно выбрать форму.  <br/> |CMainDlg::OnSelectForm  <br/> |Mfcmapi (en) использует метод **MAPIOpenFormMgr** , чтобы открыть диспетчер формы, поэтому можно выбирать в форме.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

