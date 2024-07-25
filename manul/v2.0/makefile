# ターゲットのパス（元のファイルがある場所）
SOURCE_DIR := ./firmware/manul

# 作成するディレクトリのパス
DEST_DIR := ~/GPKFW/manul

all: clean setup_firmware

# ディレクトリを作成し、ファイルをコピーするターゲット
setup_firmware:
	mkdir -p $(DEST_DIR)
	cp -R $(SOURCE_DIR)/* $(DEST_DIR)/

# 個別のファイルに対してシンボリックリンクを作成するターゲット（オプション）
create_symlinks:
	mkdir -p $(DEST_DIR)
	find $(SOURCE_DIR) -type f -exec ln -s {} $(DEST_DIR)/ \;

# クリーンアップ用のターゲット
clean:
	rm -rf $(DEST_DIR)