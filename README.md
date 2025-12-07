# karusauniverseimport datetime

# 今の日付と時間を取得
now = datetime.datetime.now()
timestamp = now.strftime("%Y年%m月%d日 %H時%M分")

# ユーザーに気分を聞く
mood = input("今の気分を入力してください: ")

# ログファイルに記録
with open("emotion_log.txt", "a", encoding="utf-8") as file:
    file.write(f"[{timestamp}] 気分: {mood}\n")

print("感情ログが記録されました！")
