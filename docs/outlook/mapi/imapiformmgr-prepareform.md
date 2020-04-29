---
title: имапиформмгрпрепареформ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416652"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Загружает форму для открытия.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Параметры

 _улуипарам_
  
> возврата Дескриптор родительского окна индикатора хода выполнения, отображаемого при загрузке формы. Параметр _улуипарам_ игнорируется, если в параметре _ulFlags_ не задан флаг MAPI_DIALOG. 
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих способ загрузки формы. Можно задать следующий флаг:
    
MAPI_DIALOG 
  
> Отображает пользовательский интерфейс для предоставления сведений о состоянии или предлагает пользователю ввести дополнительные сведения. Если этот флаг не установлен, Пользовательский интерфейс не отображается.
    
 _пфрмиинфо_
  
> возврата Указатель на объект информации формы для загружаемой формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Средства просмотра форм вызывают метод **имапиформмгр::P репареформ** для загрузки формы из контейнера формы для открытия. Большинству средству просмотра форм не требуется вызывать **препареформ**, так как методы [Имапиформмгр:: креатеформ](imapiformmgr-createform.md) и [Имапиформмгр:: лоадформ](imapiformmgr-loadform.md) вызывают **препареформ**, если это необходимо. 
  
С помощью **препареформ** можно получить библиотеки динамической компоновки (DLL) и другие файлы, связанные с формой, чтобы изменить их. Если измененная форма загружается обратно в контейнер форм, ее необходимо переустановить. 
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

