---
title: имапиформмгрселектформконтаинер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428594"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отображает диалоговое окно, позволяющее пользователю выбрать контейнер формы и возврат интерфейса для объекта контейнера, выбранного пользователем.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Параметры

 _улуипарам_
  
> возврата Дескриптор родительского окна отображаемого диалогового окна. 
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих, как выбирается Библиотека форм (то есть, как выбран контейнер форм). Можно задать следующие флаги:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> Выбор можно выполнить из всех контейнеров. Это тип выбора по умолчанию. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> Выбор можно осуществлять только из контейнеров папок.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> Выбор можно осуществлять только из контейнеров, которые не связаны с папками.
    
 _лппфкнт_
  
> вышли Указатель на указатель на возвращенный интерфейс. Этот интерфейс предназначен для объекта Container, выбранного пользователем.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Средства просмотра форм обычно вызывают метод **имапиформмгр:: селектформконтаинер** для выбора контейнера формы, в котором установлена форма. **Селектформконтаинер** не может использоваться для выбора локального контейнера форм, который имеет значение HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маиндлг. cpp  <br/> |Кмаиндлг:: Онселектформконтаинер  <br/> |MFCMAPI использует метод **имапиформмгр:: селектформконтаинер** для выбора контейнера формы перед отображением его содержимого.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

